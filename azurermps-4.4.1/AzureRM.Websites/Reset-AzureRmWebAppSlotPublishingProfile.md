---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 3CD449A1-084E-4950-80EF-06B5ECDFB70F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Reset-AzureRmWebAppSlotPublishingProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Reset-AzureRmWebAppSlotPublishingProfile.md
ms.openlocfilehash: b6a01079bed80017054e7fe52673012827dce02d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93525456"
---
# <span data-ttu-id="4ce6f-101">Reset-AzureRmWebAppSlotPublishingProfile</span><span class="sxs-lookup"><span data-stu-id="4ce6f-101">Reset-AzureRmWebAppSlotPublishingProfile</span></span>

## <span data-ttu-id="4ce6f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4ce6f-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4ce6f-103">구문과</span><span class="sxs-lookup"><span data-stu-id="4ce6f-103">SYNTAX</span></span>

### <span data-ttu-id="4ce6f-104">S1</span><span class="sxs-lookup"><span data-stu-id="4ce6f-104">S1</span></span>
```
Reset-AzureRmWebAppSlotPublishingProfile [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4ce6f-105">구성원과</span><span class="sxs-lookup"><span data-stu-id="4ce6f-105">S2</span></span>
```
Reset-AzureRmWebAppSlotPublishingProfile [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4ce6f-106">설명은</span><span class="sxs-lookup"><span data-stu-id="4ce6f-106">DESCRIPTION</span></span>
<span data-ttu-id="4ce6f-107">**AzureRmWebAppSlotPublishingProfile** cmdlet은 지정 된 웹 앱 슬롯에 대 한 게시 프로필을 초기화 합니다.</span><span class="sxs-lookup"><span data-stu-id="4ce6f-107">The **Reset-AzureRmWebAppSlotPublishingProfile** cmdlet resets the publishing profile for the specified Web App Slot.</span></span>

## <span data-ttu-id="4ce6f-108">예제의</span><span class="sxs-lookup"><span data-stu-id="4ce6f-108">EXAMPLES</span></span>

### <span data-ttu-id="4ce6f-109">raid-1</span><span class="sxs-lookup"><span data-stu-id="4ce6f-109">1:</span></span>
```
PS C:\> Reset-AzureRmWebAppSlotPublishingProfile -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "slot001"
```

<span data-ttu-id="4ce6f-110">이 명령은 리소스 그룹 Default-웹용 WestUS와 연결 된 웹 앱 ContosoWebApp의 slot001 이라는 슬롯에 대 한 게시 프로필을 다시 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4ce6f-110">This command resets the publishing profile for the Slot named slot001 for the Web App ContosoWebApp associated with the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="4ce6f-111">변수</span><span class="sxs-lookup"><span data-stu-id="4ce6f-111">PARAMETERS</span></span>

### <span data-ttu-id="4ce6f-112">-이름</span><span class="sxs-lookup"><span data-stu-id="4ce6f-112">-Name</span></span>
<span data-ttu-id="4ce6f-113">Web app 이름</span><span class="sxs-lookup"><span data-stu-id="4ce6f-113">WebApp Name</span></span>

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

### <span data-ttu-id="4ce6f-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4ce6f-114">-ResourceGroupName</span></span>
<span data-ttu-id="4ce6f-115">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="4ce6f-115">Resource Group Name</span></span>

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

### <span data-ttu-id="4ce6f-116">-슬롯</span><span class="sxs-lookup"><span data-stu-id="4ce6f-116">-Slot</span></span>
<span data-ttu-id="4ce6f-117">Web app 슬롯 이름</span><span class="sxs-lookup"><span data-stu-id="4ce6f-117">WebApp Slot Name</span></span>

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

### <span data-ttu-id="4ce6f-118">-Web app</span><span class="sxs-lookup"><span data-stu-id="4ce6f-118">-WebApp</span></span>
<span data-ttu-id="4ce6f-119">Web app 개체</span><span class="sxs-lookup"><span data-stu-id="4ce6f-119">WebApp Object</span></span>

```yaml
Type: Microsoft.Azure.Management.WebSites.Models.Site
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4ce6f-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ce6f-120">-DefaultProfile</span></span>
<span data-ttu-id="4ce6f-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="4ce6f-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ce6f-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ce6f-122">CommonParameters</span></span>
<span data-ttu-id="4ce6f-123">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="4ce6f-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ce6f-124">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4ce6f-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ce6f-125">입력</span><span class="sxs-lookup"><span data-stu-id="4ce6f-125">INPUTS</span></span>

### <span data-ttu-id="4ce6f-126">Site</span><span class="sxs-lookup"><span data-stu-id="4ce6f-126">Site</span></span>
<span data-ttu-id="4ce6f-127">' Web app ' 매개 변수는 파이프라인에서 ' Site ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="4ce6f-127">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="4ce6f-128">출력</span><span class="sxs-lookup"><span data-stu-id="4ce6f-128">OUTPUTS</span></span>

## <span data-ttu-id="4ce6f-129">상속자</span><span class="sxs-lookup"><span data-stu-id="4ce6f-129">NOTES</span></span>

## <span data-ttu-id="4ce6f-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4ce6f-130">RELATED LINKS</span></span>

