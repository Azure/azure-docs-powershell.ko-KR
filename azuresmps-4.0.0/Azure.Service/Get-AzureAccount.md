---
external help file: Microsoft.WindowsAzure.Commands.Profile.dll-Help.xml
ms.assetid: 70ADAF16-BC52-47BF-A85A-A84DEACDA027
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2704dbdc308b9773452b05ceba24719f2e274132
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045676"
---
# <span data-ttu-id="0277a-101">Get-AzureAccount</span><span class="sxs-lookup"><span data-stu-id="0277a-101">Get-AzureAccount</span></span>

## <span data-ttu-id="0277a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0277a-102">SYNOPSIS</span></span>
<span data-ttu-id="0277a-103">Azure PowerShell에 사용할 수 있는 Azure 계정을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="0277a-103">Gets Azure accounts that are available to Azure PowerShell.</span></span>

## <span data-ttu-id="0277a-104">구문과</span><span class="sxs-lookup"><span data-stu-id="0277a-104">SYNTAX</span></span>

```
Get-AzureAccount [-Name <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="0277a-105">설명은</span><span class="sxs-lookup"><span data-stu-id="0277a-105">DESCRIPTION</span></span>
<span data-ttu-id="0277a-106">**Get AzureAccount** Cmdlet은 Windows PowerShell에서 사용할 수 있는 Azure 계정을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="0277a-106">The **Get-AzureAccount** cmdlet gets the Azure accounts that are available to Windows PowerShell.</span></span>
<span data-ttu-id="0277a-107">Windows PowerShell에서 계정을 사용할 수 있게 하려면 **추가-AzureAccount** 또는 **가져오기-# 파일** cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="0277a-107">To make your accounts available to Windows PowerShell, use the **Add-AzureAccount** or **Import-PublishSettingsFile** cmdlets.</span></span>

## <span data-ttu-id="0277a-108">예제의</span><span class="sxs-lookup"><span data-stu-id="0277a-108">EXAMPLES</span></span>

### <span data-ttu-id="0277a-109">예제 1: 모든 계정 가져오기</span><span class="sxs-lookup"><span data-stu-id="0277a-109">Example 1: Get all accounts</span></span>
```
PS C:\> Get-AzureAccount

Name                         ActiveDirectories
----                         -----------------
contosoadmin@outlook.com     {{ ActiveDirectoryTenantId = abcde5cd-bcc3-441a-bd86-e6a...
contosotest1@outlook.com     {{ ActiveDirectoryTenantId = aaeabcde-386c-4466-bf70-794...
```

<span data-ttu-id="0277a-110">이 명령은 지정 된 사용자와 연결 된 모든 계정을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="0277a-110">This command gets all accounts associated with the specified user.</span></span>

### <span data-ttu-id="0277a-111">예제 2: 이름으로 계정 가져오기</span><span class="sxs-lookup"><span data-stu-id="0277a-111">Example 2: Get an account by name</span></span>
```
PS C:\> Get-AzureAccount -Name contosoadmin@outlook.com

Name                         ActiveDirectories
----                         -----------------
contosoadmin@outlook.com     {{ ActiveDirectoryTenantId = abcde5cd-bcc3-441a-bd86-e6a...
```

<span data-ttu-id="0277a-112">이 명령은 ContosoAdmin 계정을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="0277a-112">This command gets the ContosoAdmin account.</span></span>

## <span data-ttu-id="0277a-113">변수</span><span class="sxs-lookup"><span data-stu-id="0277a-113">PARAMETERS</span></span>

### <span data-ttu-id="0277a-114">-이름</span><span class="sxs-lookup"><span data-stu-id="0277a-114">-Name</span></span>
<span data-ttu-id="0277a-115">지정 된 계정만 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="0277a-115">Gets only the specified account.</span></span>
<span data-ttu-id="0277a-116">기본값은 Windows PowerShell에서 사용할 수 있는 모든 계정입니다.</span><span class="sxs-lookup"><span data-stu-id="0277a-116">The default is all accounts that are available to Windows PowerShell.</span></span>
<span data-ttu-id="0277a-117">계정 이름을 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="0277a-117">Enter the account name.</span></span>
<span data-ttu-id="0277a-118">**이름** 값은 대/소문자를 구분 합니다.</span><span class="sxs-lookup"><span data-stu-id="0277a-118">The **Name** value is case-sensitive.</span></span>
<span data-ttu-id="0277a-119">와일드 카드는 허용 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0277a-119">Wildcards are not permitted.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0277a-120">-프로필</span><span class="sxs-lookup"><span data-stu-id="0277a-120">-Profile</span></span>
<span data-ttu-id="0277a-121">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0277a-121">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="0277a-122">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="0277a-122">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="0277a-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0277a-123">CommonParameters</span></span>
<span data-ttu-id="0277a-124">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="0277a-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0277a-125">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0277a-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0277a-126">입력</span><span class="sxs-lookup"><span data-stu-id="0277a-126">INPUTS</span></span>

### <span data-ttu-id="0277a-127">않아야</span><span class="sxs-lookup"><span data-stu-id="0277a-127">None</span></span>
<span data-ttu-id="0277a-128">이 cmdlet에는 입력을 파이프가 지정할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="0277a-128">You cannot pipe input to this cmdlet.</span></span>

## <span data-ttu-id="0277a-129">출력</span><span class="sxs-lookup"><span data-stu-id="0277a-129">OUTPUTS</span></span>

### <span data-ttu-id="0277a-130">않아야</span><span class="sxs-lookup"><span data-stu-id="0277a-130">None</span></span>
<span data-ttu-id="0277a-131">이 cmdlet은 출력을 반환 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0277a-131">This cmdlet does not return any output.</span></span>

## <span data-ttu-id="0277a-132">상속자</span><span class="sxs-lookup"><span data-stu-id="0277a-132">NOTES</span></span>

## <span data-ttu-id="0277a-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0277a-133">RELATED LINKS</span></span>

[<span data-ttu-id="0277a-134">추가-AzureAccount</span><span class="sxs-lookup"><span data-stu-id="0277a-134">Add-AzureAccount</span></span>](./Add-AzureAccount.md)

[<span data-ttu-id="0277a-135">Get-Azure도움말 파일</span><span class="sxs-lookup"><span data-stu-id="0277a-135">Get-AzurePublishSettingsFile</span></span>](./Get-AzurePublishSettingsFile.md)

[<span data-ttu-id="0277a-136">가져오기-Azure# settingsfile</span><span class="sxs-lookup"><span data-stu-id="0277a-136">Import-AzurePublishSettingsFile</span></span>](./Import-AzurePublishSettingsFile.md)

[<span data-ttu-id="0277a-137">-AzureAccount 제거</span><span class="sxs-lookup"><span data-stu-id="0277a-137">Remove-AzureAccount</span></span>](./Remove-AzureAccount.md)


