---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: B2FDB54F-0318-4037-BC1D-6113E77DDE7E
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/get-azwebappslotpublishingprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppSlotPublishingProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppSlotPublishingProfile.md
ms.openlocfilehash: 249ecef690fa4eaf59e6a7de97a75d55a285b377
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98491467"
---
# <span data-ttu-id="4d074-101">Get-AzWebAppSlotPublishingProfile</span><span class="sxs-lookup"><span data-stu-id="4d074-101">Get-AzWebAppSlotPublishingProfile</span></span>

## <span data-ttu-id="4d074-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4d074-102">SYNOPSIS</span></span>
<span data-ttu-id="4d074-103">Azure 웹앱 슬롯 게시 프로필을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="4d074-103">Gets an Azure Web App slot publishing profile.</span></span>

## <span data-ttu-id="4d074-104">구문</span><span class="sxs-lookup"><span data-stu-id="4d074-104">SYNTAX</span></span>

### <span data-ttu-id="4d074-105">S1</span><span class="sxs-lookup"><span data-stu-id="4d074-105">S1</span></span>
```
Get-AzWebAppSlotPublishingProfile [[-OutputFile] <String>] [[-Format] <String>]
 [-IncludeDisasterRecoveryEndpoints] [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4d074-106">S2</span><span class="sxs-lookup"><span data-stu-id="4d074-106">S2</span></span>
```
Get-AzWebAppSlotPublishingProfile [[-OutputFile] <String>] [[-Format] <String>]
 [-IncludeDisasterRecoveryEndpoints] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4d074-107">설명</span><span class="sxs-lookup"><span data-stu-id="4d074-107">DESCRIPTION</span></span>
<span data-ttu-id="4d074-108">**Get-AzWebAppSlotPublishingProfile** cmdlet은 지정된 슬롯에 대한 웹앱 게시 프로필을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="4d074-108">The **Get-AzWebAppSlotPublishingProfile** cmdlet gets the Web App publishing profile for the specified slot.</span></span>

## <span data-ttu-id="4d074-109">예제</span><span class="sxs-lookup"><span data-stu-id="4d074-109">EXAMPLES</span></span>

### <span data-ttu-id="4d074-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="4d074-110">Example 1</span></span>
```
PS C:\> Get-AzWebAppSlotPublishingProfile -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "slot001" -Format "Ftp" -OutputFile "C:\Users\contoso\outputfile"
```

<span data-ttu-id="4d074-111">이 명령은 리소스 그룹 Default-Web-WestUS와 연결된 웹앱 ContosoWebApp과 관련된 slot Slot001에 대한 Ftp 형식의 게시 프로필을 다운로드하고 지정된 출력 파일에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="4d074-111">This command gets the publishing profile in Ftp format for slot Slot001 pertaining to the Web App ContosoWebApp associated with the resource group Default-Web-WestUS and stores it in the specified output file.</span></span>

## <span data-ttu-id="4d074-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4d074-112">PARAMETERS</span></span>

### <span data-ttu-id="4d074-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4d074-113">-DefaultProfile</span></span>
<span data-ttu-id="4d074-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="4d074-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d074-115">-Format</span><span class="sxs-lookup"><span data-stu-id="4d074-115">-Format</span></span>
<span data-ttu-id="4d074-116">서식</span><span class="sxs-lookup"><span data-stu-id="4d074-116">Format</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: WebDeploy, FileZilla3, Ftp

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d074-117">-IncludeDisasterRecoveryEndpoints</span><span class="sxs-lookup"><span data-stu-id="4d074-117">-IncludeDisasterRecoveryEndpoints</span></span>
<span data-ttu-id="4d074-118">true인 경우 재해 복구 엔드포인트 포함</span><span class="sxs-lookup"><span data-stu-id="4d074-118">Include the disaster recovery endpoints if true</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d074-119">-Name</span><span class="sxs-lookup"><span data-stu-id="4d074-119">-Name</span></span>
<span data-ttu-id="4d074-120">WebApp 이름</span><span class="sxs-lookup"><span data-stu-id="4d074-120">WebApp Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4d074-121">-OutputFile</span><span class="sxs-lookup"><span data-stu-id="4d074-121">-OutputFile</span></span>
<span data-ttu-id="4d074-122">출력 파일</span><span class="sxs-lookup"><span data-stu-id="4d074-122">Output File</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d074-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4d074-123">-ResourceGroupName</span></span>
<span data-ttu-id="4d074-124">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="4d074-124">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d074-125">-Slot</span><span class="sxs-lookup"><span data-stu-id="4d074-125">-Slot</span></span>
<span data-ttu-id="4d074-126">WebApp 슬롯 이름</span><span class="sxs-lookup"><span data-stu-id="4d074-126">WebApp Slot Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d074-127">-WebApp</span><span class="sxs-lookup"><span data-stu-id="4d074-127">-WebApp</span></span>
<span data-ttu-id="4d074-128">WebApp 개체</span><span class="sxs-lookup"><span data-stu-id="4d074-128">WebApp Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.PSSite
Parameter Sets: S2
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4d074-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d074-129">CommonParameters</span></span>
<span data-ttu-id="4d074-130">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="4d074-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d074-131">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="4d074-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d074-132">입력</span><span class="sxs-lookup"><span data-stu-id="4d074-132">INPUTS</span></span>

### <span data-ttu-id="4d074-133">System.String</span><span class="sxs-lookup"><span data-stu-id="4d074-133">System.String</span></span>

### <span data-ttu-id="4d074-134">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="4d074-134">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="4d074-135">출력</span><span class="sxs-lookup"><span data-stu-id="4d074-135">OUTPUTS</span></span>

### <span data-ttu-id="4d074-136">System.String</span><span class="sxs-lookup"><span data-stu-id="4d074-136">System.String</span></span>

## <span data-ttu-id="4d074-137">참고 사항</span><span class="sxs-lookup"><span data-stu-id="4d074-137">NOTES</span></span>

## <span data-ttu-id="4d074-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4d074-138">RELATED LINKS</span></span>

[<span data-ttu-id="4d074-139">Reset-AzWebAppSlotPublishingProfile</span><span class="sxs-lookup"><span data-stu-id="4d074-139">Reset-AzWebAppSlotPublishingProfile</span></span>](./Reset-AzWebAppSlotPublishingProfile.md)

[<span data-ttu-id="4d074-140">Get-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="4d074-140">Get-AzWebAppSlot</span></span>](./Get-AzWebAppSlot.md)

[<span data-ttu-id="4d074-141">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="4d074-141">Get-AzWebApp</span></span>](./Get-AzWebApp.md)
