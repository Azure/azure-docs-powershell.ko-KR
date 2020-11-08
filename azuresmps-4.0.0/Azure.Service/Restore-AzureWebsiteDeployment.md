---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: B83ABF05-3169-4D05-AB6E-167DE045595D
online version: ''
schema: 2.0.0
ms.openlocfilehash: fea9341b288b5c2f98413cc95cb42bffe1a78ca3
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045463"
---
# <span data-ttu-id="56aa7-101">Restore-AzureWebsiteDeployment</span><span class="sxs-lookup"><span data-stu-id="56aa7-101">Restore-AzureWebsiteDeployment</span></span>

## <span data-ttu-id="56aa7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="56aa7-102">SYNOPSIS</span></span>
<span data-ttu-id="56aa7-103">Azure에서 이전 웹 사이트 배포를 다시 배포 합니다.</span><span class="sxs-lookup"><span data-stu-id="56aa7-103">Redeploys a previous deployment of a website in Azure.</span></span>

## <span data-ttu-id="56aa7-104">구문과</span><span class="sxs-lookup"><span data-stu-id="56aa7-104">SYNTAX</span></span>

```
Restore-AzureWebsiteDeployment [-CommitId <String>] [-Force] [-Name <String>] [-Slot <String>]
 [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="56aa7-105">설명은</span><span class="sxs-lookup"><span data-stu-id="56aa7-105">DESCRIPTION</span></span>
<span data-ttu-id="56aa7-106">이 항목에서는 0.8.10 버전의 Microsoft Azure PowerShell 모듈에 대 한 cmdlet에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="56aa7-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="56aa7-107">사용 중인 모듈 버전을 Azure PowerShell 콘솔에 가져오려면 다음을 입력 `(Get-Module -Name Azure).Version` 합니다.</span><span class="sxs-lookup"><span data-stu-id="56aa7-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="56aa7-108">**AzureWebsiteDeployment** Cmdlet은 Azure에서 이전 웹 사이트 배포를 다시 배포 합니다.</span><span class="sxs-lookup"><span data-stu-id="56aa7-108">The **Restore-AzureWebsiteDeployment** cmdlet redeploys a previous deployment of a website in Azure.</span></span>
<span data-ttu-id="56aa7-109">이 프로세스는 현재 배포를 선택한 배포로 바꿉니다.</span><span class="sxs-lookup"><span data-stu-id="56aa7-109">This process replaces the current deployment with the selected deployment.</span></span>

## <span data-ttu-id="56aa7-110">예제의</span><span class="sxs-lookup"><span data-stu-id="56aa7-110">EXAMPLES</span></span>

### <span data-ttu-id="56aa7-111">예제 1: 사이트 다시 배포</span><span class="sxs-lookup"><span data-stu-id="56aa7-111">Example 1: Redeploy a site</span></span>
```
PS C:\> Restore-AzureWebsiteDeployment -Name "ContosoSite" -CommitId "f876543210"
```

<span data-ttu-id="56aa7-112">이 명령은 ContosoSite 이라는 웹 사이트의 ID f876543210 인 배포를 다시 배포 합니다.</span><span class="sxs-lookup"><span data-stu-id="56aa7-112">This command redeploys the deployment that has the ID f876543210 for the website named ContosoSite.</span></span>

## <span data-ttu-id="56aa7-113">변수</span><span class="sxs-lookup"><span data-stu-id="56aa7-113">PARAMETERS</span></span>

### <span data-ttu-id="56aa7-114">-CommitId</span><span class="sxs-lookup"><span data-stu-id="56aa7-114">-CommitId</span></span>
<span data-ttu-id="56aa7-115">다시 배포할 배포의 식별자를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="56aa7-115">Specifies the identifier of the deployment to redeploy.</span></span>

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

### <span data-ttu-id="56aa7-116">-Force</span><span class="sxs-lookup"><span data-stu-id="56aa7-116">-Force</span></span>
<span data-ttu-id="56aa7-117">이 기능을 사용 하는 경우 확인 메시지를 표시 하지 않고 이전 배포를 다시 배포 합니다.</span><span class="sxs-lookup"><span data-stu-id="56aa7-117">If enabled, redeploys the previous deployment without prompting for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56aa7-118">-이름</span><span class="sxs-lookup"><span data-stu-id="56aa7-118">-Name</span></span>
<span data-ttu-id="56aa7-119">다시 배포할 웹 사이트의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="56aa7-119">Specifies the name of the website to redeploy.</span></span>

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

### <span data-ttu-id="56aa7-120">-프로필</span><span class="sxs-lookup"><span data-stu-id="56aa7-120">-Profile</span></span>
<span data-ttu-id="56aa7-121">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="56aa7-121">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="56aa7-122">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="56aa7-122">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="56aa7-123">-슬롯</span><span class="sxs-lookup"><span data-stu-id="56aa7-123">-Slot</span></span>
<span data-ttu-id="56aa7-124">슬롯 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="56aa7-124">Specifies the slot name.</span></span>

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

### <span data-ttu-id="56aa7-125">-확인</span><span class="sxs-lookup"><span data-stu-id="56aa7-125">-Confirm</span></span>
<span data-ttu-id="56aa7-126">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="56aa7-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56aa7-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="56aa7-127">-WhatIf</span></span>
<span data-ttu-id="56aa7-128">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="56aa7-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="56aa7-129">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="56aa7-129">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56aa7-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56aa7-130">CommonParameters</span></span>
<span data-ttu-id="56aa7-131">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="56aa7-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56aa7-132">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="56aa7-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56aa7-133">입력</span><span class="sxs-lookup"><span data-stu-id="56aa7-133">INPUTS</span></span>

## <span data-ttu-id="56aa7-134">출력</span><span class="sxs-lookup"><span data-stu-id="56aa7-134">OUTPUTS</span></span>

## <span data-ttu-id="56aa7-135">상속자</span><span class="sxs-lookup"><span data-stu-id="56aa7-135">NOTES</span></span>

## <span data-ttu-id="56aa7-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="56aa7-136">RELATED LINKS</span></span>

[<span data-ttu-id="56aa7-137">Get-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="56aa7-137">Get-AzureWebsite</span></span>](./Get-AzureWebsite.md)

[<span data-ttu-id="56aa7-138">Get-AzureWebsiteDeployment</span><span class="sxs-lookup"><span data-stu-id="56aa7-138">Get-AzureWebsiteDeployment</span></span>](./Get-AzureWebsiteDeployment.md)


