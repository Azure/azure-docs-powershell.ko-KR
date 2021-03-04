---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: B2FDB54F-0318-4037-BC1D-6113E77DDE7E
online version: https://docs.microsoft.com/powershell/module/az.websites/get-azwebappslotpublishingprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppSlotPublishingProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppSlotPublishingProfile.md
ms.openlocfilehash: fed1be90af7aad2126b20dbe830f5069cc62e01f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101994658"
---
# <span data-ttu-id="5319c-101">Get-AzWebAppSlotPublishingProfile</span><span class="sxs-lookup"><span data-stu-id="5319c-101">Get-AzWebAppSlotPublishingProfile</span></span>

## <span data-ttu-id="5319c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5319c-102">SYNOPSIS</span></span>
<span data-ttu-id="5319c-103">Azure Web App 슬롯 게시 프로필을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="5319c-103">Gets an Azure Web App slot publishing profile.</span></span>

## <span data-ttu-id="5319c-104">구문</span><span class="sxs-lookup"><span data-stu-id="5319c-104">SYNTAX</span></span>

### <span data-ttu-id="5319c-105">S1</span><span class="sxs-lookup"><span data-stu-id="5319c-105">S1</span></span>
```
Get-AzWebAppSlotPublishingProfile [[-OutputFile] <String>] [[-Format] <String>]
 [-IncludeDisasterRecoveryEndpoints] [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5319c-106">S2</span><span class="sxs-lookup"><span data-stu-id="5319c-106">S2</span></span>
```
Get-AzWebAppSlotPublishingProfile [[-OutputFile] <String>] [[-Format] <String>]
 [-IncludeDisasterRecoveryEndpoints] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5319c-107">설명</span><span class="sxs-lookup"><span data-stu-id="5319c-107">DESCRIPTION</span></span>
<span data-ttu-id="5319c-108">**Get-AzWebAppSlotPublishingProfile** cmdlet은 지정된 슬롯에 대한 웹앱 게시 프로필을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="5319c-108">The **Get-AzWebAppSlotPublishingProfile** cmdlet gets the Web App publishing profile for the specified slot.</span></span>

## <span data-ttu-id="5319c-109">예제</span><span class="sxs-lookup"><span data-stu-id="5319c-109">EXAMPLES</span></span>

### <span data-ttu-id="5319c-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="5319c-110">Example 1</span></span>
```
PS C:\> Get-AzWebAppSlotPublishingProfile -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "slot001" -Format "Ftp" -OutputFile "C:\Users\contoso\outputfile"
```

<span data-ttu-id="5319c-111">이 명령은 리소스 그룹 Default-Web-WestUS와 연결된 Web App ContosoWebApp에 관련된 슬롯 슬롯001의 Ftp 형식의 게시 프로필을 얻게 하여 지정된 출력 파일에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="5319c-111">This command gets the publishing profile in Ftp format for slot Slot001 pertaining to the Web App ContosoWebApp associated with the resource group Default-Web-WestUS and stores it in the specified output file.</span></span>

## <span data-ttu-id="5319c-112">매개 변수</span><span class="sxs-lookup"><span data-stu-id="5319c-112">PARAMETERS</span></span>

### <span data-ttu-id="5319c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5319c-113">-DefaultProfile</span></span>
<span data-ttu-id="5319c-114">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="5319c-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5319c-115">-Format</span><span class="sxs-lookup"><span data-stu-id="5319c-115">-Format</span></span>
<span data-ttu-id="5319c-116">서식</span><span class="sxs-lookup"><span data-stu-id="5319c-116">Format</span></span>

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

### <span data-ttu-id="5319c-117">-IncludeDisasterRecoveryEndpoints</span><span class="sxs-lookup"><span data-stu-id="5319c-117">-IncludeDisasterRecoveryEndpoints</span></span>
<span data-ttu-id="5319c-118">true인 경우 재해 복구 엔드포인트 포함</span><span class="sxs-lookup"><span data-stu-id="5319c-118">Include the disaster recovery endpoints if true</span></span>

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

### <span data-ttu-id="5319c-119">-Name</span><span class="sxs-lookup"><span data-stu-id="5319c-119">-Name</span></span>
<span data-ttu-id="5319c-120">WebApp 이름</span><span class="sxs-lookup"><span data-stu-id="5319c-120">WebApp Name</span></span>

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

### <span data-ttu-id="5319c-121">-OutputFile</span><span class="sxs-lookup"><span data-stu-id="5319c-121">-OutputFile</span></span>
<span data-ttu-id="5319c-122">출력 파일</span><span class="sxs-lookup"><span data-stu-id="5319c-122">Output File</span></span>

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

### <span data-ttu-id="5319c-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5319c-123">-ResourceGroupName</span></span>
<span data-ttu-id="5319c-124">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="5319c-124">Resource Group Name</span></span>

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

### <span data-ttu-id="5319c-125">-Slot</span><span class="sxs-lookup"><span data-stu-id="5319c-125">-Slot</span></span>
<span data-ttu-id="5319c-126">WebApp 슬롯 이름</span><span class="sxs-lookup"><span data-stu-id="5319c-126">WebApp Slot Name</span></span>

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

### <span data-ttu-id="5319c-127">-WebApp</span><span class="sxs-lookup"><span data-stu-id="5319c-127">-WebApp</span></span>
<span data-ttu-id="5319c-128">WebApp 개체</span><span class="sxs-lookup"><span data-stu-id="5319c-128">WebApp Object</span></span>

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

### <span data-ttu-id="5319c-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5319c-129">CommonParameters</span></span>
<span data-ttu-id="5319c-130">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="5319c-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5319c-131">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="5319c-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5319c-132">입력</span><span class="sxs-lookup"><span data-stu-id="5319c-132">INPUTS</span></span>

### <span data-ttu-id="5319c-133">System.String</span><span class="sxs-lookup"><span data-stu-id="5319c-133">System.String</span></span>

### <span data-ttu-id="5319c-134">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="5319c-134">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="5319c-135">출력</span><span class="sxs-lookup"><span data-stu-id="5319c-135">OUTPUTS</span></span>

### <span data-ttu-id="5319c-136">System.String</span><span class="sxs-lookup"><span data-stu-id="5319c-136">System.String</span></span>

## <span data-ttu-id="5319c-137">참고 사항</span><span class="sxs-lookup"><span data-stu-id="5319c-137">NOTES</span></span>

## <span data-ttu-id="5319c-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5319c-138">RELATED LINKS</span></span>

[<span data-ttu-id="5319c-139">Reset-AzWebAppSlotPublishingProfile</span><span class="sxs-lookup"><span data-stu-id="5319c-139">Reset-AzWebAppSlotPublishingProfile</span></span>](./Reset-AzWebAppSlotPublishingProfile.md)

[<span data-ttu-id="5319c-140">Get-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="5319c-140">Get-AzWebAppSlot</span></span>](./Get-AzWebAppSlot.md)

[<span data-ttu-id="5319c-141">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="5319c-141">Get-AzWebApp</span></span>](./Get-AzWebApp.md)
