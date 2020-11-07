---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorhealthprobesettingobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorHealthProbeSettingObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorHealthProbeSettingObject.md
ms.openlocfilehash: 60eaa3b5482d6d1c13236560f797383d68d97b44
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93689885"
---
# <span data-ttu-id="0b089-101">New-AzFrontDoorHealthProbeSettingObject</span><span class="sxs-lookup"><span data-stu-id="0b089-101">New-AzFrontDoorHealthProbeSettingObject</span></span>

## <span data-ttu-id="0b089-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0b089-102">SYNOPSIS</span></span>
<span data-ttu-id="0b089-103">전방 도어 만들기에 대 한 PSHealthProbeSetting 개체 만들기</span><span class="sxs-lookup"><span data-stu-id="0b089-103">Create a PSHealthProbeSetting object for Front Door creation</span></span>

## <span data-ttu-id="0b089-104">구문과</span><span class="sxs-lookup"><span data-stu-id="0b089-104">SYNTAX</span></span>

```
New-AzFrontDoorHealthProbeSettingObject -Name <String> [-Path <String>] [-Protocol <PSProtocol>]
 [-IntervalInSeconds <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0b089-105">설명은</span><span class="sxs-lookup"><span data-stu-id="0b089-105">DESCRIPTION</span></span>
<span data-ttu-id="0b089-106">전방 도어 만들기에 대 한 PSHealthProbeSetting 개체 만들기</span><span class="sxs-lookup"><span data-stu-id="0b089-106">Create a PSHealthProbeSetting object for Front Door creation</span></span>

## <span data-ttu-id="0b089-107">예제의</span><span class="sxs-lookup"><span data-stu-id="0b089-107">EXAMPLES</span></span>

### <span data-ttu-id="0b089-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="0b089-108">Example 1</span></span>
```powershell
PS C:\>  New-AzFrontDoorHealthProbeSettingObject -Name "healthProbeSetting1"


Path              : /
Protocol          : Http
IntervalInSeconds : 30
ResourceState     :
Id                :
Name              : healthProbeSetting1
Type              :
```

<span data-ttu-id="0b089-109">전방 도어 만들기에 대 한 PSHealthProbeSetting 개체 만들기</span><span class="sxs-lookup"><span data-stu-id="0b089-109">Create a PSHealthProbeSetting object for Front Door creation</span></span>

## <span data-ttu-id="0b089-110">변수</span><span class="sxs-lookup"><span data-stu-id="0b089-110">PARAMETERS</span></span>

### <span data-ttu-id="0b089-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0b089-111">-DefaultProfile</span></span>
<span data-ttu-id="0b089-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="0b089-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0b089-113">-IntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="0b089-113">-IntervalInSeconds</span></span>
<span data-ttu-id="0b089-114">상태 프로브 사이의 초 수입니다.</span><span class="sxs-lookup"><span data-stu-id="0b089-114">The number of seconds between health probes.</span></span>
<span data-ttu-id="0b089-115">기본값은 30입니다.</span><span class="sxs-lookup"><span data-stu-id="0b089-115">Default value is 30</span></span>

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

### <span data-ttu-id="0b089-116">-이름</span><span class="sxs-lookup"><span data-stu-id="0b089-116">-Name</span></span>
<span data-ttu-id="0b089-117">상태 검색 설정 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0b089-117">health probe setting name.</span></span>

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

### <span data-ttu-id="0b089-118">-Path</span><span class="sxs-lookup"><span data-stu-id="0b089-118">-Path</span></span>
<span data-ttu-id="0b089-119">상태 프로브에 사용할 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="0b089-119">The path to use for the health probe.</span></span>
<span data-ttu-id="0b089-120">기본값은/</span><span class="sxs-lookup"><span data-stu-id="0b089-120">Default is /</span></span>

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

### <span data-ttu-id="0b089-121">-프로토콜</span><span class="sxs-lookup"><span data-stu-id="0b089-121">-Protocol</span></span>
<span data-ttu-id="0b089-122">이 프로브 기본값에 사용할 프로토콜 스키마는 HTTP입니다.</span><span class="sxs-lookup"><span data-stu-id="0b089-122">Protocol scheme to use for this probe Default value is HTTP</span></span>

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

### <span data-ttu-id="0b089-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b089-123">CommonParameters</span></span>
<span data-ttu-id="0b089-124">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="0b089-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b089-125">자세한 내용은 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="0b089-125">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b089-126">입력</span><span class="sxs-lookup"><span data-stu-id="0b089-126">INPUTS</span></span>

### <span data-ttu-id="0b089-127">않아야</span><span class="sxs-lookup"><span data-stu-id="0b089-127">None</span></span>

## <span data-ttu-id="0b089-128">출력</span><span class="sxs-lookup"><span data-stu-id="0b089-128">OUTPUTS</span></span>

### <span data-ttu-id="0b089-129">FrontDoor. PSHealthProbeSetting/.</span><span class="sxs-lookup"><span data-stu-id="0b089-129">Microsoft.Azure.Commands.FrontDoor.Models.PSHealthProbeSetting</span></span>

## <span data-ttu-id="0b089-130">상속자</span><span class="sxs-lookup"><span data-stu-id="0b089-130">NOTES</span></span>

## <span data-ttu-id="0b089-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0b089-131">RELATED LINKS</span></span>

<span data-ttu-id="0b089-132">[새로운 AzFrontDoor](./New-AzFrontDoor.md) 
 [Set-AzFrontDoor](./Set-AzFrontDoor.md)</span><span class="sxs-lookup"><span data-stu-id="0b089-132">[New-AzFrontDoor](./New-AzFrontDoor.md)
[Set-AzFrontDoor](./Set-AzFrontDoor.md)</span></span>
