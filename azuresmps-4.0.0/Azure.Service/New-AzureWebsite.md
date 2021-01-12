---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: FBB55071-454D-4473-93BA-D97F33067785
online version: ''
schema: 2.0.0
ms.openlocfilehash: 768eff2dda32c6dfa0bad14f028338d3c5fa1abd
ms.sourcegitcommit: 87730c7ea4f98f628d3fe1b40aa4a9d2885e1c75
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/12/2021
ms.locfileid: "98110481"
---
# <span data-ttu-id="953e4-101">New-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="953e4-101">New-AzureWebsite</span></span>

## <span data-ttu-id="953e4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="953e4-102">SYNOPSIS</span></span>
<span data-ttu-id="953e4-103">Azure에서 실행할 새 웹 사이트를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="953e4-103">Create a new website to run in Azure.</span></span>

## <span data-ttu-id="953e4-104">구문</span><span class="sxs-lookup"><span data-stu-id="953e4-104">SYNTAX</span></span>

```
New-AzureWebsite [-Location <String>] [-Hostname <String>] [-PublishingUsername <String>] [-Git] [-GitHub]
 [-GitHubCredentials <PSCredential>] [-GitHubRepository <String>] [-Name <String>] [-Slot <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="953e4-105">설명</span><span class="sxs-lookup"><span data-stu-id="953e4-105">DESCRIPTION</span></span>
<span data-ttu-id="953e4-106">이 항목에서는 Microsoft Azure PowerShell 모듈의 0.8.10 버전 cmdlet에 대해 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="953e4-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="953e4-107">사용 하는 모듈의 버전을 얻습니다. Azure PowerShell 콘솔에서 를 `(Get-Module -Name Azure).Version` 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="953e4-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="953e4-108">cmdlet은 Azure에서 실행할 새 웹 사이트를 만들고 GitHub를 통해 배포를 준비합니다.</span><span class="sxs-lookup"><span data-stu-id="953e4-108">The cmdlet creates a new website to run in Azure and prepares for deployment through GitHub.</span></span>

## <span data-ttu-id="953e4-109">예제</span><span class="sxs-lookup"><span data-stu-id="953e4-109">EXAMPLES</span></span>

### <span data-ttu-id="953e4-110">예제 1: Git를 사용하여 새 웹 사이트 만들기</span><span class="sxs-lookup"><span data-stu-id="953e4-110">Example 1: Create a new website with Git</span></span>
```
PS C:\> New-AzureWebsite mySite -Git
```

<span data-ttu-id="953e4-111">이 예제에서는 새 웹 사이트에 파일을 배포하는 데 사용할 Azure 및 로컬 Git 리포지토리에 새 웹 사이트를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="953e4-111">This example creates a new website in Azure and a local Git repository to use for deploying files to the new website.</span></span>

### <span data-ttu-id="953e4-112">예제 2: GitHub와 통합된 웹 사이트 만들기</span><span class="sxs-lookup"><span data-stu-id="953e4-112">Example 2: Create website integrated with GitHub</span></span>
```
PS C:\> New-AzureWebsite mysite -GitHub -GitHubRepository myaccount/myrepo
```

<span data-ttu-id="953e4-113">이 예제에서는 myaccount/myrepo라는 GitHub 리포지토리에 연결된 새 웹 사이트를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="953e4-113">This example creates a new website linked to a GitHub repository named myaccount/myrepo.</span></span>
<span data-ttu-id="953e4-114">GitHub 리포지토리에 대한 커밋은 Azure의 웹 사이트로 푸시됩니다.</span><span class="sxs-lookup"><span data-stu-id="953e4-114">Commits to the GitHub repository are pushed to the website in Azure.</span></span>

## <span data-ttu-id="953e4-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="953e4-115">PARAMETERS</span></span>

### <span data-ttu-id="953e4-116">-Git</span><span class="sxs-lookup"><span data-stu-id="953e4-116">-Git</span></span>
<span data-ttu-id="953e4-117">로컬 Git 리포지토리를 설정하고 웹 사이트에 연결합니다.</span><span class="sxs-lookup"><span data-stu-id="953e4-117">Sets up a local Git repository and links it to the website.</span></span>
<span data-ttu-id="953e4-118">지정된 경우 이 매개 변수는 로컬 디렉터리에서 Git 리포지토리를 설정하고 Azure의 웹 사이트에 연결되는 'azure'라는 원격 리포지토리를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="953e4-118">If specified, this parameter sets up a Git repository in the local directory and add a remote repository named 'azure' that links to the website in Azure.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="953e4-119">-GitHub</span><span class="sxs-lookup"><span data-stu-id="953e4-119">-GitHub</span></span>
<span data-ttu-id="953e4-120">이 cmdlet은 새 웹 사이트를 기존 GitHub 리포지토리에 연결합니다.</span><span class="sxs-lookup"><span data-stu-id="953e4-120">Indicates that this cmdlet links the new website to an existing GitHub repository.</span></span>
<span data-ttu-id="953e4-121">Giuthub 리포지토리에 대한 커밋은 Azure의 웹 사이트로 푸시됩니다.</span><span class="sxs-lookup"><span data-stu-id="953e4-121">Commits to the Giuthub repository are pushed to the website in Azure.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="953e4-122">-GitHubCredentials</span><span class="sxs-lookup"><span data-stu-id="953e4-122">-GitHubCredentials</span></span>
<span data-ttu-id="953e4-123">GitHub에 연결할 사용자 이름 및 암호 자격 증명을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="953e4-123">Specifies the user name and password credentials to connect to GitHub.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="953e4-124">-GitHubRepository</span><span class="sxs-lookup"><span data-stu-id="953e4-124">-GitHubRepository</span></span>
<span data-ttu-id="953e4-125">이 웹 사이트에 연결하기 위해 GitHub 리포지토리의 전체 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="953e4-125">Specifies the full name of the GitHub repository to link to this website.</span></span>
<span data-ttu-id="953e4-126">예: `myaccount/myrepo`</span><span class="sxs-lookup"><span data-stu-id="953e4-126">For example, `myaccount/myrepo`.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="953e4-127">-Hostname</span><span class="sxs-lookup"><span data-stu-id="953e4-127">-Hostname</span></span>
<span data-ttu-id="953e4-128">새 웹 사이트의 대체 호스트 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="953e4-128">Specifies an alternative host name for the new website.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="953e4-129">-Location</span><span class="sxs-lookup"><span data-stu-id="953e4-129">-Location</span></span>
<span data-ttu-id="953e4-130">웹 사이트를 배포하려는 데이터 센터의 위치를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="953e4-130">Specifies the location of the data center where you want to deploy the website.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="953e4-131">-Name</span><span class="sxs-lookup"><span data-stu-id="953e4-131">-Name</span></span>
<span data-ttu-id="953e4-132">웹 사이트의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="953e4-132">Specifies a name for the website.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="953e4-133">-Profile</span><span class="sxs-lookup"><span data-stu-id="953e4-133">-Profile</span></span>
<span data-ttu-id="953e4-134">이 cmdlet이 읽을 Azure 프로필을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="953e4-134">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="953e4-135">프로필을 지정하지 않으면 이 cmdlet은 로컬 기본 프로필에서 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="953e4-135">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="953e4-136">-PublishingUsername</span><span class="sxs-lookup"><span data-stu-id="953e4-136">-PublishingUsername</span></span>
<span data-ttu-id="953e4-137">Git 배포용 Azure Portal에서 지정한 사용자 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="953e4-137">Specifies the user name you have specified in the Azure Portal for Git deployment.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="953e4-138">-Slot</span><span class="sxs-lookup"><span data-stu-id="953e4-138">-Slot</span></span>
<span data-ttu-id="953e4-139">웹 사이트의 슬롯 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="953e4-139">Specifies a slot name for the website.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="953e4-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="953e4-140">CommonParameters</span></span>
<span data-ttu-id="953e4-141">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="953e4-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="953e4-142">자세한 내용은 다음 about_CommonParameters https://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="953e4-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="953e4-143">입력</span><span class="sxs-lookup"><span data-stu-id="953e4-143">INPUTS</span></span>

## <span data-ttu-id="953e4-144">출력</span><span class="sxs-lookup"><span data-stu-id="953e4-144">OUTPUTS</span></span>

## <span data-ttu-id="953e4-145">참고 사항</span><span class="sxs-lookup"><span data-stu-id="953e4-145">NOTES</span></span>

## <span data-ttu-id="953e4-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="953e4-146">RELATED LINKS</span></span>

[<span data-ttu-id="953e4-147">Set-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="953e4-147">Set-AzureWebsite</span></span>](./Set-AzureWebsite.md)


