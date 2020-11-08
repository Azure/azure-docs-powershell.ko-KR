---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: B2FDB54F-0318-4037-BC1D-6113E77DDE7E
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/get-azwebappslotpublishingprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppSlotPublishingProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppSlotPublishingProfile.md
ms.openlocfilehash: 249ecef690fa4eaf59e6a7de97a75d55a285b377
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94217126"
---
# <span data-ttu-id="fcb41-101">Get-AzWebAppSlotPublishingProfile</span><span class="sxs-lookup"><span data-stu-id="fcb41-101">Get-AzWebAppSlotPublishingProfile</span></span>

## <span data-ttu-id="fcb41-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fcb41-102">SYNOPSIS</span></span>
<span data-ttu-id="fcb41-103">Azure 웹 앱 슬롯 게시 프로필을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="fcb41-103">Gets an Azure Web App slot publishing profile.</span></span>

## <span data-ttu-id="fcb41-104">구문과</span><span class="sxs-lookup"><span data-stu-id="fcb41-104">SYNTAX</span></span>

### <span data-ttu-id="fcb41-105">S1</span><span class="sxs-lookup"><span data-stu-id="fcb41-105">S1</span></span>
```
Get-AzWebAppSlotPublishingProfile [[-OutputFile] <String>] [[-Format] <String>]
 [-IncludeDisasterRecoveryEndpoints] [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fcb41-106">구성원과</span><span class="sxs-lookup"><span data-stu-id="fcb41-106">S2</span></span>
```
Get-AzWebAppSlotPublishingProfile [[-OutputFile] <String>] [[-Format] <String>]
 [-IncludeDisasterRecoveryEndpoints] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="fcb41-107">설명은</span><span class="sxs-lookup"><span data-stu-id="fcb41-107">DESCRIPTION</span></span>
<span data-ttu-id="fcb41-108">**AzWebAppSlotPublishingProfile** cmdlet은 지정 된 슬롯에 대 한 Web App 게시 프로필을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="fcb41-108">The **Get-AzWebAppSlotPublishingProfile** cmdlet gets the Web App publishing profile for the specified slot.</span></span>

## <span data-ttu-id="fcb41-109">예제의</span><span class="sxs-lookup"><span data-stu-id="fcb41-109">EXAMPLES</span></span>

### <span data-ttu-id="fcb41-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="fcb41-110">Example 1</span></span>
```
PS C:\> Get-AzWebAppSlotPublishingProfile -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "slot001" -Format "Ftp" -OutputFile "C:\Users\contoso\outputfile"
```

<span data-ttu-id="fcb41-111">이 명령은 리소스 그룹 Default-Slot001에 연결 된 웹 앱 ContosoWebApp에 대 한 게시 프로필을 Ftp 형식으로 가져와 지정 된 출력 파일에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="fcb41-111">This command gets the publishing profile in Ftp format for slot Slot001 pertaining to the Web App ContosoWebApp associated with the resource group Default-Web-WestUS and stores it in the specified output file.</span></span>

## <span data-ttu-id="fcb41-112">변수</span><span class="sxs-lookup"><span data-stu-id="fcb41-112">PARAMETERS</span></span>

### <span data-ttu-id="fcb41-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fcb41-113">-DefaultProfile</span></span>
<span data-ttu-id="fcb41-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="fcb41-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fcb41-115">-형식</span><span class="sxs-lookup"><span data-stu-id="fcb41-115">-Format</span></span>
<span data-ttu-id="fcb41-116">포맷할</span><span class="sxs-lookup"><span data-stu-id="fcb41-116">Format</span></span>

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

### <span data-ttu-id="fcb41-117">-IncludeDisasterRecoveryEndpoints</span><span class="sxs-lookup"><span data-stu-id="fcb41-117">-IncludeDisasterRecoveryEndpoints</span></span>
<span data-ttu-id="fcb41-118">True 인 경우 재해 복구 끝점 포함</span><span class="sxs-lookup"><span data-stu-id="fcb41-118">Include the disaster recovery endpoints if true</span></span>

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

### <span data-ttu-id="fcb41-119">-이름</span><span class="sxs-lookup"><span data-stu-id="fcb41-119">-Name</span></span>
<span data-ttu-id="fcb41-120">Web app 이름</span><span class="sxs-lookup"><span data-stu-id="fcb41-120">WebApp Name</span></span>

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

### <span data-ttu-id="fcb41-121">-OutputFile</span><span class="sxs-lookup"><span data-stu-id="fcb41-121">-OutputFile</span></span>
<span data-ttu-id="fcb41-122">출력 파일</span><span class="sxs-lookup"><span data-stu-id="fcb41-122">Output File</span></span>

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

### <span data-ttu-id="fcb41-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fcb41-123">-ResourceGroupName</span></span>
<span data-ttu-id="fcb41-124">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="fcb41-124">Resource Group Name</span></span>

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

### <span data-ttu-id="fcb41-125">-슬롯</span><span class="sxs-lookup"><span data-stu-id="fcb41-125">-Slot</span></span>
<span data-ttu-id="fcb41-126">Web app 슬롯 이름</span><span class="sxs-lookup"><span data-stu-id="fcb41-126">WebApp Slot Name</span></span>

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

### <span data-ttu-id="fcb41-127">-Web app</span><span class="sxs-lookup"><span data-stu-id="fcb41-127">-WebApp</span></span>
<span data-ttu-id="fcb41-128">Web app 개체</span><span class="sxs-lookup"><span data-stu-id="fcb41-128">WebApp Object</span></span>

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

### <span data-ttu-id="fcb41-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fcb41-129">CommonParameters</span></span>
<span data-ttu-id="fcb41-130">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="fcb41-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fcb41-131">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fcb41-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fcb41-132">입력</span><span class="sxs-lookup"><span data-stu-id="fcb41-132">INPUTS</span></span>

### <span data-ttu-id="fcb41-133">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="fcb41-133">System.String</span></span>

### <span data-ttu-id="fcb41-134">Microsoft Azure. \*. m a i m Apps.</span><span class="sxs-lookup"><span data-stu-id="fcb41-134">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="fcb41-135">출력</span><span class="sxs-lookup"><span data-stu-id="fcb41-135">OUTPUTS</span></span>

### <span data-ttu-id="fcb41-136">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="fcb41-136">System.String</span></span>

## <span data-ttu-id="fcb41-137">상속자</span><span class="sxs-lookup"><span data-stu-id="fcb41-137">NOTES</span></span>

## <span data-ttu-id="fcb41-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="fcb41-138">RELATED LINKS</span></span>

[<span data-ttu-id="fcb41-139">다시 설정-AzWebAppSlotPublishingProfile</span><span class="sxs-lookup"><span data-stu-id="fcb41-139">Reset-AzWebAppSlotPublishingProfile</span></span>](./Reset-AzWebAppSlotPublishingProfile.md)

[<span data-ttu-id="fcb41-140">Get-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="fcb41-140">Get-AzWebAppSlot</span></span>](./Get-AzWebAppSlot.md)

[<span data-ttu-id="fcb41-141">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="fcb41-141">Get-AzWebApp</span></span>](./Get-AzWebApp.md)
