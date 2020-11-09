---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzSecurityAdaptiveApplicationControlGroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAdaptiveApplicationControlGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAdaptiveApplicationControlGroup.md
ms.openlocfilehash: 9d36169439a2466ca50858f5b438822461259cf3
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94311084"
---
# <span data-ttu-id="75be9-101">Get-AzSecurityAdaptiveApplicationControlGroup</span><span class="sxs-lookup"><span data-stu-id="75be9-101">Get-AzSecurityAdaptiveApplicationControlGroup</span></span>

## <span data-ttu-id="75be9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="75be9-102">SYNOPSIS</span></span>
<span data-ttu-id="75be9-103">응용 프로그램 컨트롤 VM/서버 그룹을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="75be9-103">Gets an application control VM/server group.</span></span>

## <span data-ttu-id="75be9-104">구문과</span><span class="sxs-lookup"><span data-stu-id="75be9-104">SYNTAX</span></span>

### <span data-ttu-id="75be9-105">구독 범위 (기본값)</span><span class="sxs-lookup"><span data-stu-id="75be9-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecurityAdaptiveApplicationControlGroup  -GroupName <String> -AscLocation <String> [-SubscriptionId <String>]
[-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="75be9-106">설명은</span><span class="sxs-lookup"><span data-stu-id="75be9-106">DESCRIPTION</span></span>
<span data-ttu-id="75be9-107">적응 응용 프로그램 컨트롤은 Azure 보안 센터에서 자동으로 계산 되며,이 cmdlet을 사용 하 여 응용 프로그램 컨트롤 VM/서버 그룹을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="75be9-107">Adaptive Application Controls are automatically calculated by Azure Security Center, use this cmdlet to get an application control VM/server group.</span></span>

## <span data-ttu-id="75be9-108">예제의</span><span class="sxs-lookup"><span data-stu-id="75be9-108">EXAMPLES</span></span>

### <span data-ttu-id="75be9-109">예제 1</span><span class="sxs-lookup"><span data-stu-id="75be9-109">Example 1</span></span>
```powershell
PS C:\> Get-AzSecurityAdaptiveApplicationControlGroup -GroupName GROUP1 -AscLocation centralus
Id         : /subscriptions/3eeab341-f466-499c-a8be-85427e154baf7612f869/providers/Microsoft.Security/locations/centralus/applicationWhitelistings/GROUP1
Name       : GROUP1
Type       : Microsoft.Security/applicationWhitelistings
Location   : centralus
Properties : Microsoft.Azure.Commands.SecurityCenter.Models.AdaptiveApplicationControls.PSSecurityAdaptiveApplicationControlsProperties
```
<span data-ttu-id="75be9-110">응용 프로그램 컨트롤 VM/서버 그룹을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="75be9-110">Gets an application control VM/server group.</span></span>


## <span data-ttu-id="75be9-111">변수</span><span class="sxs-lookup"><span data-stu-id="75be9-111">PARAMETERS</span></span>

### <span data-ttu-id="75be9-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75be9-112">-DefaultProfile</span></span>
<span data-ttu-id="75be9-113">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="75be9-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="75be9-114">-AscLocation</span><span class="sxs-lookup"><span data-stu-id="75be9-114">-AscLocation</span></span>
<span data-ttu-id="75be9-115">ASC에서 구독의 데이터를 저장 하는 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="75be9-115">The location where ASC stores the data of the subscription.</span></span> <span data-ttu-id="75be9-116">Get 위치에서 검색할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="75be9-116">can be retrieved from Get locations.</span></span>

```yaml
Type: System.String
Parameter Sets: AscLocation
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75be9-117">-GroupName</span><span class="sxs-lookup"><span data-stu-id="75be9-117">-GroupName</span></span>
<span data-ttu-id="75be9-118">응용 프로그램 컨트롤 VM/서버 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="75be9-118">Name of an application control VM/server group.</span></span>

```yaml
Type: System.String
Parameter Sets: GroupName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75be9-119">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="75be9-119">-SubscriptionId</span></span>
<span data-ttu-id="75be9-120">Azure 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="75be9-120">Azure subscription ID.</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```


### <span data-ttu-id="75be9-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75be9-121">CommonParameters</span></span>
<span data-ttu-id="75be9-122">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="75be9-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75be9-123">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="75be9-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75be9-124">입력</span><span class="sxs-lookup"><span data-stu-id="75be9-124">INPUTS</span></span>

### <span data-ttu-id="75be9-125">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="75be9-125">System.String</span></span>

## <span data-ttu-id="75be9-126">출력</span><span class="sxs-lookup"><span data-stu-id="75be9-126">OUTPUTS</span></span>

### <span data-ttu-id="75be9-127">AdaptiveApplicationControls. PSSecurityAdaptiveApplicationControls에 대 한 Microsoft</span><span class="sxs-lookup"><span data-stu-id="75be9-127">Microsoft.Azure.Commands.Security.Models.AdaptiveApplicationControls.PSSecurityAdaptiveApplicationControls</span></span>

## <span data-ttu-id="75be9-128">상속자</span><span class="sxs-lookup"><span data-stu-id="75be9-128">NOTES</span></span>

## <span data-ttu-id="75be9-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="75be9-129">RELATED LINKS</span></span>