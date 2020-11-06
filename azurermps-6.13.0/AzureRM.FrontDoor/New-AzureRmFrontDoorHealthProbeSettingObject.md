---
external help file: Microsoft.Azure.Commands.FrontDoor.dll-Help.xml
Module Name: AzureRM.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.frontdoor/new-azurermfrontdoorhealthprobesettingobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/New-AzureRmFrontDoorHealthProbeSettingObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/New-AzureRmFrontDoorHealthProbeSettingObject.md
ms.openlocfilehash: dcaf61b9001093d25f351d03e8e50da4c4ca22ca
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93530329"
---
# <span data-ttu-id="0d6cf-101">New-AzureRmFrontDoorHealthProbeSettingObject</span><span class="sxs-lookup"><span data-stu-id="0d6cf-101">New-AzureRmFrontDoorHealthProbeSettingObject</span></span>

## <span data-ttu-id="0d6cf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0d6cf-102">SYNOPSIS</span></span>
<span data-ttu-id="0d6cf-103">전방 도어 만들기에 대 한 PSHealthProbeSetting 개체 만들기</span><span class="sxs-lookup"><span data-stu-id="0d6cf-103">Create a PSHealthProbeSetting object for Front Door creation</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0d6cf-104">구문과</span><span class="sxs-lookup"><span data-stu-id="0d6cf-104">SYNTAX</span></span>

```
New-AzureRmFrontDoorHealthProbeSettingObject -Name <String> [-Path <String>] [-Protocol <PSProtocol>]
 [-IntervalInSeconds <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0d6cf-105">설명은</span><span class="sxs-lookup"><span data-stu-id="0d6cf-105">DESCRIPTION</span></span>
<span data-ttu-id="0d6cf-106">전방 도어 만들기에 대 한 PSHealthProbeSetting 개체 만들기</span><span class="sxs-lookup"><span data-stu-id="0d6cf-106">Create a PSHealthProbeSetting object for Front Door creation</span></span>

## <span data-ttu-id="0d6cf-107">예제의</span><span class="sxs-lookup"><span data-stu-id="0d6cf-107">EXAMPLES</span></span>

### <span data-ttu-id="0d6cf-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="0d6cf-108">Example 1</span></span>
```powershell
PS C:\>  New-AzureRmFrontDoorHealthProbeSettingObject -Name "healthProbeSetting1"


Path              : /
Protocol          : Http
IntervalInSeconds : 30
ResourceState     :
Id                :
Name              : healthProbeSetting1
Type              :
```

<span data-ttu-id="0d6cf-109">전방 도어 만들기에 대 한 PSHealthProbeSetting 개체 만들기</span><span class="sxs-lookup"><span data-stu-id="0d6cf-109">Create a PSHealthProbeSetting object for Front Door creation</span></span>

## <span data-ttu-id="0d6cf-110">변수</span><span class="sxs-lookup"><span data-stu-id="0d6cf-110">PARAMETERS</span></span>

### <span data-ttu-id="0d6cf-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d6cf-111">-DefaultProfile</span></span>
<span data-ttu-id="0d6cf-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="0d6cf-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0d6cf-113">-IntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="0d6cf-113">-IntervalInSeconds</span></span>
<span data-ttu-id="0d6cf-114">상태 프로브 사이의 초 수입니다.</span><span class="sxs-lookup"><span data-stu-id="0d6cf-114">The number of seconds between health probes.</span></span>
<span data-ttu-id="0d6cf-115">기본값은 30입니다.</span><span class="sxs-lookup"><span data-stu-id="0d6cf-115">Default value is 30</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d6cf-116">-이름</span><span class="sxs-lookup"><span data-stu-id="0d6cf-116">-Name</span></span>
<span data-ttu-id="0d6cf-117">상태 검색 설정 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0d6cf-117">health probe setting name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d6cf-118">-Path</span><span class="sxs-lookup"><span data-stu-id="0d6cf-118">-Path</span></span>
<span data-ttu-id="0d6cf-119">상태 프로브에 사용할 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="0d6cf-119">The path to use for the health probe.</span></span>
<span data-ttu-id="0d6cf-120">기본값은/</span><span class="sxs-lookup"><span data-stu-id="0d6cf-120">Default is /</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d6cf-121">-프로토콜</span><span class="sxs-lookup"><span data-stu-id="0d6cf-121">-Protocol</span></span>
<span data-ttu-id="0d6cf-122">이 프로브 기본값에 사용할 프로토콜 스키마는 HTTP입니다.</span><span class="sxs-lookup"><span data-stu-id="0d6cf-122">Protocol scheme to use for this probe Default value is HTTP</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSProtocol
Parameter Sets: (All)
Aliases:
Accepted values: Http, Https

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d6cf-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d6cf-123">CommonParameters</span></span>
<span data-ttu-id="0d6cf-124">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="0d6cf-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d6cf-125">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0d6cf-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d6cf-126">입력</span><span class="sxs-lookup"><span data-stu-id="0d6cf-126">INPUTS</span></span>

### <span data-ttu-id="0d6cf-127">않아야</span><span class="sxs-lookup"><span data-stu-id="0d6cf-127">None</span></span>

## <span data-ttu-id="0d6cf-128">출력</span><span class="sxs-lookup"><span data-stu-id="0d6cf-128">OUTPUTS</span></span>

### <span data-ttu-id="0d6cf-129">FrontDoor. PSHealthProbeSetting/.</span><span class="sxs-lookup"><span data-stu-id="0d6cf-129">Microsoft.Azure.Commands.FrontDoor.Models.PSHealthProbeSetting</span></span>

## <span data-ttu-id="0d6cf-130">상속자</span><span class="sxs-lookup"><span data-stu-id="0d6cf-130">NOTES</span></span>

## <span data-ttu-id="0d6cf-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0d6cf-131">RELATED LINKS</span></span>

<span data-ttu-id="0d6cf-132">[새로운 AzureRmFrontDoor](./New-AzureRmFrontDoor.md) 
 [Set-AzureRmFrontDoor](./Set-AzureRmFrontDoor.md)</span><span class="sxs-lookup"><span data-stu-id="0d6cf-132">[New-AzureRmFrontDoor](./New-AzureRmFrontDoor.md)
[Set-AzureRmFrontDoor](./Set-AzureRmFrontDoor.md)</span></span>
