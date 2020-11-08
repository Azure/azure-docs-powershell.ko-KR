---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: FBB55071-454D-4473-93BA-D97F33067785
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0f83489d21fba97bb50145de1fedc1ac9a7195a1
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046184"
---
# <span data-ttu-id="516cd-101">New-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="516cd-101">New-AzureWebsite</span></span>

## <span data-ttu-id="516cd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="516cd-102">SYNOPSIS</span></span>
<span data-ttu-id="516cd-103">Azure에서 실행할 새 웹 사이트를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="516cd-103">Create a new website to run in Azure.</span></span>

## <span data-ttu-id="516cd-104">구문과</span><span class="sxs-lookup"><span data-stu-id="516cd-104">SYNTAX</span></span>

```
New-AzureWebsite [-Location <String>] [-Hostname <String>] [-PublishingUsername <String>] [-Git] [-GitHub]
 [-GithubCredentials <PSCredential>] [-GithubRepository <String>] [-Name <String>] [-Slot <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="516cd-105">설명은</span><span class="sxs-lookup"><span data-stu-id="516cd-105">DESCRIPTION</span></span>
<span data-ttu-id="516cd-106">이 항목에서는 0.8.10 버전의 Microsoft Azure PowerShell 모듈에 대 한 cmdlet에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="516cd-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="516cd-107">사용 중인 모듈 버전을 Azure PowerShell 콘솔에 가져오려면 다음을 입력 `(Get-Module -Name Azure).Version` 합니다.</span><span class="sxs-lookup"><span data-stu-id="516cd-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="516cd-108">Cmdlet은 Azure에서 실행할 새 웹 사이트를 만들고 Github를 통해 배포를 준비 합니다.</span><span class="sxs-lookup"><span data-stu-id="516cd-108">The cmdlet creates a new website to run in Azure and prepares for deployment through Github.</span></span>

## <span data-ttu-id="516cd-109">예제의</span><span class="sxs-lookup"><span data-stu-id="516cd-109">EXAMPLES</span></span>

### <span data-ttu-id="516cd-110">예제 1: Git을 사용 하 여 새 웹 사이트 만들기</span><span class="sxs-lookup"><span data-stu-id="516cd-110">Example 1: Create a new website with Git</span></span>
```
PS C:\> New-AzureWebsite mySite -Git
```

<span data-ttu-id="516cd-111">이 예제에서는 Azure에 새 웹 사이트를 만들고 새 웹 사이트에 파일을 배포 하는 데 사용할 로컬 Git 리포지토리를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="516cd-111">This example creates a new website in Azure and a local Git repository to use for deploying files to the new website.</span></span>

### <span data-ttu-id="516cd-112">예제 2: Github와 통합 된 웹 사이트 만들기</span><span class="sxs-lookup"><span data-stu-id="516cd-112">Example 2: Create website integrated with Github</span></span>
```
PS C:\> New-AzureWebsite mysite -Github -GithubRepository myaccount/myrepo
```

<span data-ttu-id="516cd-113">이 예제에서는 내 계정/myrepo 이라는 Github 리포지토리에 연결 된 새 웹 사이트를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="516cd-113">This example creates a new website linked to a Github repository named myaccount/myrepo.</span></span>
<span data-ttu-id="516cd-114">Github 리포지토리에 대 한 커밋이 Azure의 웹 사이트로 푸시됩니다.</span><span class="sxs-lookup"><span data-stu-id="516cd-114">Commits to the Github repository are pushed to the website in Azure.</span></span>

## <span data-ttu-id="516cd-115">변수</span><span class="sxs-lookup"><span data-stu-id="516cd-115">PARAMETERS</span></span>

### <span data-ttu-id="516cd-116">-Git</span><span class="sxs-lookup"><span data-stu-id="516cd-116">-Git</span></span>
<span data-ttu-id="516cd-117">로컬 Git 리포지토리를 설정 하 고 웹 사이트에 연결 합니다.</span><span class="sxs-lookup"><span data-stu-id="516cd-117">Sets up a local Git repository and links it to the website.</span></span>
<span data-ttu-id="516cd-118">지정 하는 경우이 매개 변수는 로컬 디렉터리에 Git 리포지토리를 설정 하 고 Azure의 웹 사이트에 연결 되는 ' azure ' 라는 원격 리포지토리를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="516cd-118">If specified, this parameter sets up a Git repository in the local directory and add a remote repository named 'azure' that links to the website in Azure.</span></span>

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

### <span data-ttu-id="516cd-119">-GitHub</span><span class="sxs-lookup"><span data-stu-id="516cd-119">-GitHub</span></span>
<span data-ttu-id="516cd-120">이 cmdlet이 새 웹 사이트를 기존 Github 리포지토리에 연결 하는 것을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="516cd-120">Indicates that this cmdlet links the new website to an existing Github repository.</span></span>
<span data-ttu-id="516cd-121">Giuthub 저장소에 대 한 커밋이 Azure의 웹 사이트로 푸시됩니다.</span><span class="sxs-lookup"><span data-stu-id="516cd-121">Commits to the Giuthub repository are pushed to the website in Azure.</span></span>

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

### <span data-ttu-id="516cd-122">-Gid 자격 증명</span><span class="sxs-lookup"><span data-stu-id="516cd-122">-GithubCredentials</span></span>
<span data-ttu-id="516cd-123">Github에 연결 하는 데 사용 되는 사용자 이름 및 암호 자격 증명을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="516cd-123">Specifies the user name and password credentials to connect to Github.</span></span>

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

### <span data-ttu-id="516cd-124">-GithubRepository</span><span class="sxs-lookup"><span data-stu-id="516cd-124">-GithubRepository</span></span>
<span data-ttu-id="516cd-125">이 웹 사이트에 연결할 Github 리포지토리의 전체 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="516cd-125">Specifies the full name of the Github repository to link to this website.</span></span>
<span data-ttu-id="516cd-126">예를 들어 `myaccount/myrepo` .</span><span class="sxs-lookup"><span data-stu-id="516cd-126">For example, `myaccount/myrepo`.</span></span>

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

### <span data-ttu-id="516cd-127">-Hostname</span><span class="sxs-lookup"><span data-stu-id="516cd-127">-Hostname</span></span>
<span data-ttu-id="516cd-128">새 웹 사이트의 대체 호스트 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="516cd-128">Specifies an alternative host name for the new website.</span></span>

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

### <span data-ttu-id="516cd-129">-위치</span><span class="sxs-lookup"><span data-stu-id="516cd-129">-Location</span></span>
<span data-ttu-id="516cd-130">웹 사이트를 배포 하려는 데이터 센터의 위치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="516cd-130">Specifies the location of the data center where you want to deploy the website.</span></span>

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

### <span data-ttu-id="516cd-131">-이름</span><span class="sxs-lookup"><span data-stu-id="516cd-131">-Name</span></span>
<span data-ttu-id="516cd-132">웹 사이트의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="516cd-132">Specifies a name for the website.</span></span>

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

### <span data-ttu-id="516cd-133">-프로필</span><span class="sxs-lookup"><span data-stu-id="516cd-133">-Profile</span></span>
<span data-ttu-id="516cd-134">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="516cd-134">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="516cd-135">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="516cd-135">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="516cd-136">-PublishingUsername</span><span class="sxs-lookup"><span data-stu-id="516cd-136">-PublishingUsername</span></span>
<span data-ttu-id="516cd-137">Git 배포용 Azure 포털에서 지정한 사용자 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="516cd-137">Specifies the user name you have specified in the Azure Portal for Git deployment.</span></span>

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

### <span data-ttu-id="516cd-138">-슬롯</span><span class="sxs-lookup"><span data-stu-id="516cd-138">-Slot</span></span>
<span data-ttu-id="516cd-139">웹 사이트의 슬롯 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="516cd-139">Specifies a slot name for the website.</span></span>

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

### <span data-ttu-id="516cd-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="516cd-140">CommonParameters</span></span>
<span data-ttu-id="516cd-141">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="516cd-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="516cd-142">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="516cd-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="516cd-143">입력</span><span class="sxs-lookup"><span data-stu-id="516cd-143">INPUTS</span></span>

## <span data-ttu-id="516cd-144">출력</span><span class="sxs-lookup"><span data-stu-id="516cd-144">OUTPUTS</span></span>

## <span data-ttu-id="516cd-145">상속자</span><span class="sxs-lookup"><span data-stu-id="516cd-145">NOTES</span></span>

## <span data-ttu-id="516cd-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="516cd-146">RELATED LINKS</span></span>

[<span data-ttu-id="516cd-147">Set-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="516cd-147">Set-AzureWebsite</span></span>](./Set-AzureWebsite.md)


