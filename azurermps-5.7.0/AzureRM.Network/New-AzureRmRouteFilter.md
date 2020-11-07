---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermroutefilter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmRouteFilter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmRouteFilter.md
ms.openlocfilehash: 9ba5f47427dc8f542e1475a8431f5d82c63c5974
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93711147"
---
# <span data-ttu-id="e7b3d-101">New-AzureRmRouteFilter</span><span class="sxs-lookup"><span data-stu-id="e7b3d-101">New-AzureRmRouteFilter</span></span>

## <span data-ttu-id="e7b3d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e7b3d-102">SYNOPSIS</span></span>
<span data-ttu-id="e7b3d-103">경로 필터를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e7b3d-103">Creates a route filter.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e7b3d-104">구문과</span><span class="sxs-lookup"><span data-stu-id="e7b3d-104">SYNTAX</span></span>

```
New-AzureRmRouteFilter -Name <String> -ResourceGroupName <String> -Location <String>
 [-Rule <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSRouteFilterRule]>]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e7b3d-105">설명은</span><span class="sxs-lookup"><span data-stu-id="e7b3d-105">DESCRIPTION</span></span>
<span data-ttu-id="e7b3d-106">New-AzureRmRouteFilter cmdlet은 Azure 경로 필터를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e7b3d-106">The New-AzureRmRouteFilter cmdlet creates an Azure route filter.</span></span>

## <span data-ttu-id="e7b3d-107">예제의</span><span class="sxs-lookup"><span data-stu-id="e7b3d-107">EXAMPLES</span></span>

### <span data-ttu-id="e7b3d-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="e7b3d-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

 
<span data-ttu-id="e7b3d-109">{{여기에 예제 설명 추가}}</span><span class="sxs-lookup"><span data-stu-id="e7b3d-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="e7b3d-110">변수</span><span class="sxs-lookup"><span data-stu-id="e7b3d-110">PARAMETERS</span></span>

### <span data-ttu-id="e7b3d-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e7b3d-111">-AsJob</span></span>
<span data-ttu-id="e7b3d-112">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="e7b3d-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e7b3d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e7b3d-113">-DefaultProfile</span></span>
<span data-ttu-id="e7b3d-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e7b3d-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7b3d-115">-Force</span><span class="sxs-lookup"><span data-stu-id="e7b3d-115">-Force</span></span>
<span data-ttu-id="e7b3d-116">이름이 같은 경로 필터가 이미 있는 경우에도이 cmdlet이 경로 테이블을 생성 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="e7b3d-116">Indicates that this cmdlet creates a route table even if a route filter that has the same name already exists.</span></span>

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

### <span data-ttu-id="e7b3d-117">-위치</span><span class="sxs-lookup"><span data-stu-id="e7b3d-117">-Location</span></span>
<span data-ttu-id="e7b3d-118">이 cmdlet이 경로 필터를 만드는 Azure 지역을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e7b3d-118">Specifies the Azure region in which this cmdlet creates a route filter.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7b3d-119">-이름</span><span class="sxs-lookup"><span data-stu-id="e7b3d-119">-Name</span></span>
<span data-ttu-id="e7b3d-120">경로 필터의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e7b3d-120">Specifies a name for the route filter.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7b3d-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e7b3d-121">-ResourceGroupName</span></span>
<span data-ttu-id="e7b3d-122">이 cmdlet이 경로 필터를 만드는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e7b3d-122">Specifies the name of the resource group in which this cmdlet creates a route filter.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7b3d-123">-규칙</span><span class="sxs-lookup"><span data-stu-id="e7b3d-123">-Rule</span></span>
<span data-ttu-id="e7b3d-124">경로 필터와 연결할 경로 필터 규칙 개체의 배열을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e7b3d-124">Specifies an array of Route Filter Rule objects to associate with the route filter.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSRouteFilterRule]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7b3d-125">태그</span><span class="sxs-lookup"><span data-stu-id="e7b3d-125">-Tag</span></span>
<span data-ttu-id="e7b3d-126">해시 테이블 형태의 키-값 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="e7b3d-126">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="e7b3d-127">예를 들어:</span><span class="sxs-lookup"><span data-stu-id="e7b3d-127">For example:</span></span>

<span data-ttu-id="e7b3d-128">@ {key0 = "value0", key1 = $null, key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="e7b3d-128">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7b3d-129">-확인</span><span class="sxs-lookup"><span data-stu-id="e7b3d-129">-Confirm</span></span>
<span data-ttu-id="e7b3d-130">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="e7b3d-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7b3d-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e7b3d-131">-WhatIf</span></span>
<span data-ttu-id="e7b3d-132">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="e7b3d-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e7b3d-133">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e7b3d-133">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7b3d-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7b3d-134">CommonParameters</span></span>
<span data-ttu-id="e7b3d-135">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e7b3d-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7b3d-136">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e7b3d-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7b3d-137">입력</span><span class="sxs-lookup"><span data-stu-id="e7b3d-137">INPUTS</span></span>

### <span data-ttu-id="e7b3d-138">않아야</span><span class="sxs-lookup"><span data-stu-id="e7b3d-138">None</span></span>
<span data-ttu-id="e7b3d-139">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e7b3d-139">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="e7b3d-140">출력</span><span class="sxs-lookup"><span data-stu-id="e7b3d-140">OUTPUTS</span></span>

### <span data-ttu-id="e7b3d-141">PSRouteFilter에 대 한.</span><span class="sxs-lookup"><span data-stu-id="e7b3d-141">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="e7b3d-142">상속자</span><span class="sxs-lookup"><span data-stu-id="e7b3d-142">NOTES</span></span>
<span data-ttu-id="e7b3d-143">키워드: azure, azurerm, arm, resource, 관리, 관리자, 네트워크, 네트워킹</span><span class="sxs-lookup"><span data-stu-id="e7b3d-143">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="e7b3d-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e7b3d-144">RELATED LINKS</span></span>

[<span data-ttu-id="e7b3d-145">Get-AzureRmRouteFilter</span><span class="sxs-lookup"><span data-stu-id="e7b3d-145">Get-AzureRmRouteFilter</span></span>](./Get-AzureRmRouteFilter.md)

[<span data-ttu-id="e7b3d-146">새로운 AzureRmRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="e7b3d-146">New-AzureRmRouteFilterRuleConfig</span></span>](./New-AzureRmRouteFilterRuleConfig.md)

[<span data-ttu-id="e7b3d-147">제거-AzureRmRouteFilter</span><span class="sxs-lookup"><span data-stu-id="e7b3d-147">Remove-AzureRmRouteFilter</span></span>](./Remove-AzureRmRouteFilter.md)

[<span data-ttu-id="e7b3d-148">Set-AzureRmRouteFilter</span><span class="sxs-lookup"><span data-stu-id="e7b3d-148">Set-AzureRmRouteFilter</span></span>](./Set-AzureRmRouteFilter.md)
