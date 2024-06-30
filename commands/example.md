const { SlashCommandBuilder } = require('discord.js');

module.exports = {
  data: new SlashCommandBuilder()
    .setName('mycommand')          // Command name (lowercase without spaces)
    .setDescription('Description of your command'),  // Command description

  async execute(interaction) {
    // Logic for your command goes here
    try {
      // Example response: Reply with a simple text
      await interaction.reply('This is my custom command!');
    } catch (error) {
      console.error('Error executing command:', error);
      await interaction.reply({ content: 'There was an error executing this command!', ephemeral: true });
    }
  },
};
