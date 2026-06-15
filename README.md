# README.md

## Document Your Vision

```bash
```

## Load Skill Files

```bash
# prepare the project directory
mkdir -p  ~/tmp/electronics_primer/.claude/skills

# install superpowers

# install skill files
CURRENT_DIR=$PWD
SOURCE_DIR=~/src/projects/makersmiths/skills
TARGET_DIR=~/tmp/electronics_primer/.claude/skills
cd $SOURCE_DIR/course_skills ; cp -r * $TARGET_DIR ; cd $CURRENT_DIR
cd $SOURCE_DIR/questioning_skills ; cp -r * $TARGET_DIR ; cd $CURRENT_DIR
cd $SOURCE_DIR/writing_skills ; cp -r * $TARGET_DIR ; cd $CURRENT_DIR
```

## Initialize Claude Code
Start with the following after entering Claude Code:

```bash
# clear claude code's contest
/clear

# initialize the CLAUDE.md file
/init

# set model to opus
/model opus

# use planning mode
/plan

# work hard
/effort high
```


