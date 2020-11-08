---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 3CD449A1-084E-4950-80EF-06B5ECDFB70F
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/reset-azwebappslotpublishingprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Reset-AzWebAppSlotPublishingProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Reset-AzWebAppSlotPublishingProfile.md
ms.openlocfilehash: 8670581b376fe185ae4e477524f8f0a01c7cd3a0
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94042916"
---
# <span data-ttu-id="67c7b-101">Reset-AzWebAppSlotPublishingProfile</span><span class="sxs-lookup"><span data-stu-id="67c7b-101">Reset-AzWebAppSlotPublishingProfile</span></span>

## <span data-ttu-id="67c7b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="67c7b-102">SYNOPSIS</span></span>

## <span data-ttu-id="67c7b-103">구문과</span><span class="sxs-lookup"><span data-stu-id="67c7b-103">SYNTAX</span></span>

### <span data-ttu-id="67c7b-104">S1</span><span class="sxs-lookup"><span data-stu-id="67c7b-104">S1</span></span>
```
Reset-AzWebAppSlotPublishingProfile [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="67c7b-105">구성원과</span><span class="sxs-lookup"><span data-stu-id="67c7b-105">S2</span></span>
```
Reset-AzWebAppSlotPublishingProfile [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="67c7b-106">설명은</span><span class="sxs-lookup"><span data-stu-id="67c7b-106">DESCRIPTION</span></span>
<span data-ttu-id="67c7b-107">**AzWebAppSlotPublishingProfile** cmdlet은 지정 된 웹 앱 슬롯에 대 한 게시 프로필을 초기화 합니다.</span><span class="sxs-lookup"><span data-stu-id="67c7b-107">The **Reset-AzWebAppSlotPublishingProfile** cmdlet resets the publishing profile for the specified Web App Slot.</span></span>

## <span data-ttu-id="67c7b-108">예제의</span><span class="sxs-lookup"><span data-stu-id="67c7b-108">EXAMPLES</span></span>

### <span data-ttu-id="67c7b-109">raid-1</span><span class="sxs-lookup"><span data-stu-id="67c7b-109">1:</span></span>
```
PS C:\> Reset-AzWebAppSlotPublishingProfile -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "slot001"
```

<span data-ttu-id="67c7b-110">이 명령은 리소스 그룹 Default-웹용 WestUS와 연결 된 웹 앱 ContosoWebApp의 slot001 이라는 슬롯에 대 한 게시 프로필을 다시 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="67c7b-110">This command resets the publishing profile for the Slot named slot001 for the Web App ContosoWebApp associated with the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="67c7b-111">변수</span><span class="sxs-lookup"><span data-stu-id="67c7b-111">PARAMETERS</span></span>

### <span data-ttu-id="67c7b-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67c7b-112">-DefaultProfile</span></span>
<span data-ttu-id="67c7b-113">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="67c7b-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="67c7b-114">-이름</span><span class="sxs-lookup"><span data-stu-id="67c7b-114">-Name</span></span>
<span data-ttu-id="67c7b-115">Web app 이름</span><span class="sxs-lookup"><span data-stu-id="67c7b-115">WebApp Name</span></span>

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

### <span data-ttu-id="67c7b-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="67c7b-116">-ResourceGroupName</span></span>
<span data-ttu-id="67c7b-117">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="67c7b-117">Resource Group Name</span></span>

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

### <span data-ttu-id="67c7b-118">-슬롯</span><span class="sxs-lookup"><span data-stu-id="67c7b-118">-Slot</span></span>
<span data-ttu-id="67c7b-119">Web app 슬롯 이름</span><span class="sxs-lookup"><span data-stu-id="67c7b-119">WebApp Slot Name</span></span>

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

### <span data-ttu-id="67c7b-120">-Web app</span><span class="sxs-lookup"><span data-stu-id="67c7b-120">-WebApp</span></span>
<span data-ttu-id="67c7b-121">Web app 개체</span><span class="sxs-lookup"><span data-stu-id="67c7b-121">WebApp Object</span></span>

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

### <span data-ttu-id="67c7b-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67c7b-122">CommonParameters</span></span>
<span data-ttu-id="67c7b-123">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="67c7b-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67c7b-124">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="67c7b-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67c7b-125">입력</span><span class="sxs-lookup"><span data-stu-id="67c7b-125">INPUTS</span></span>

### <span data-ttu-id="67c7b-126">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="67c7b-126">System.String</span></span>

### <span data-ttu-id="67c7b-127">Microsoft Azure. \*. m a i m Apps.</span><span class="sxs-lookup"><span data-stu-id="67c7b-127">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="67c7b-128">출력</span><span class="sxs-lookup"><span data-stu-id="67c7b-128">OUTPUTS</span></span>

### <span data-ttu-id="67c7b-129">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="67c7b-129">System.String</span></span>

## <span data-ttu-id="67c7b-130">상속자</span><span class="sxs-lookup"><span data-stu-id="67c7b-130">NOTES</span></span>

## <span data-ttu-id="67c7b-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="67c7b-131">RELATED LINKS</span></span>