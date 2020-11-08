---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/remove-azpeeringregisteredasn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Remove-AzPeeringRegisteredAsn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Remove-AzPeeringRegisteredAsn.md
ms.openlocfilehash: d43fe033b58ba6295728bc0c21ddb1d853587b59
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94216033"
---
# <span data-ttu-id="a79fe-101">Remove-AzPeeringRegisteredAsn</span><span class="sxs-lookup"><span data-stu-id="a79fe-101">Remove-AzPeeringRegisteredAsn</span></span>

## <span data-ttu-id="a79fe-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a79fe-102">SYNOPSIS</span></span>
<span data-ttu-id="a79fe-103">부모 피어 링 리소스에서 등록 된 ASN을 삭제 하거나 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="a79fe-103">Delete or remove a registered ASN from the parent peering resource.</span></span>

## <span data-ttu-id="a79fe-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a79fe-104">SYNTAX</span></span>

### <span data-ttu-id="a79fe-105">ByName (기본값)</span><span class="sxs-lookup"><span data-stu-id="a79fe-105">ByName (Default)</span></span>
```
Remove-AzPeeringRegisteredAsn [-ResourceGroupName] <String> [-PeeringName] <String> [-Name] <String> [-Force]
 [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a79fe-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="a79fe-106">InputObject</span></span>
```
Remove-AzPeeringRegisteredAsn -InputObject <PSPeeringServicePrefix> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a79fe-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="a79fe-107">ByResourceId</span></span>
```
Remove-AzPeeringRegisteredAsn [-ResourceId] <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a79fe-108">설명은</span><span class="sxs-lookup"><span data-stu-id="a79fe-108">DESCRIPTION</span></span>
<span data-ttu-id="a79fe-109">부모 피어 링 리소스에서 등록 된 ASN을 제거할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a79fe-109">Allows the removal of registered ASN from parent peering resource.</span></span>

## <span data-ttu-id="a79fe-110">예제의</span><span class="sxs-lookup"><span data-stu-id="a79fe-110">EXAMPLES</span></span>

### <span data-ttu-id="a79fe-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="a79fe-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzPeeringRegisteredAsn -ResourceId $resourceId
```

<span data-ttu-id="a79fe-112">리소스 id를 기준으로 registerd ASN을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="a79fe-112">Remove a registerd ASN by resource id.</span></span>

## <span data-ttu-id="a79fe-113">변수</span><span class="sxs-lookup"><span data-stu-id="a79fe-113">PARAMETERS</span></span>

### <span data-ttu-id="a79fe-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a79fe-114">-AsJob</span></span>
<span data-ttu-id="a79fe-115">백그라운드에서 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="a79fe-115">Run in the background.</span></span>

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

### <span data-ttu-id="a79fe-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a79fe-116">-DefaultProfile</span></span>
<span data-ttu-id="a79fe-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a79fe-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a79fe-118">-Force</span><span class="sxs-lookup"><span data-stu-id="a79fe-118">-Force</span></span>
<span data-ttu-id="a79fe-119">강제로 작업 완료</span><span class="sxs-lookup"><span data-stu-id="a79fe-119">Force the operation to complete</span></span>

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

### <span data-ttu-id="a79fe-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a79fe-120">-InputObject</span></span>
<span data-ttu-id="a79fe-121">Get-AzPeeringServicePrefix 사용</span><span class="sxs-lookup"><span data-stu-id="a79fe-121">Use a Get-AzPeeringServicePrefix</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringServicePrefix
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a79fe-122">-이름</span><span class="sxs-lookup"><span data-stu-id="a79fe-122">-Name</span></span>
<span data-ttu-id="a79fe-123">등록 된 ASN의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a79fe-123">The name of the registered ASN</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a79fe-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a79fe-124">-PassThru</span></span>
<span data-ttu-id="a79fe-125">{{Fill PassThru 설명}}</span><span class="sxs-lookup"><span data-stu-id="a79fe-125">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="a79fe-126">-PeeringName</span><span class="sxs-lookup"><span data-stu-id="a79fe-126">-PeeringName</span></span>
<span data-ttu-id="a79fe-127">PSPeering의 고유 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a79fe-127">The unique name of the PSPeering.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a79fe-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a79fe-128">-ResourceGroupName</span></span>
<span data-ttu-id="a79fe-129">기존 리소스 그룹 이름을 만들거나 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="a79fe-129">The create or use an existing resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a79fe-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a79fe-130">-ResourceId</span></span>
<span data-ttu-id="a79fe-131">리소스 id 문자열 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a79fe-131">The resource id string name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a79fe-132">-확인</span><span class="sxs-lookup"><span data-stu-id="a79fe-132">-Confirm</span></span>
<span data-ttu-id="a79fe-133">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="a79fe-133">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a79fe-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a79fe-134">-WhatIf</span></span>
<span data-ttu-id="a79fe-135">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="a79fe-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a79fe-136">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a79fe-136">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a79fe-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a79fe-137">CommonParameters</span></span>
<span data-ttu-id="a79fe-138">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a79fe-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a79fe-139">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="a79fe-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a79fe-140">입력</span><span class="sxs-lookup"><span data-stu-id="a79fe-140">INPUTS</span></span>

### <span data-ttu-id="a79fe-141">PSPeeringServicePrefix (Microsoft. PowerShell.</span><span class="sxs-lookup"><span data-stu-id="a79fe-141">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringServicePrefix</span></span>

### <span data-ttu-id="a79fe-142">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="a79fe-142">System.String</span></span>

## <span data-ttu-id="a79fe-143">출력</span><span class="sxs-lookup"><span data-stu-id="a79fe-143">OUTPUTS</span></span>

### <span data-ttu-id="a79fe-144">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="a79fe-144">System.Boolean</span></span>

## <span data-ttu-id="a79fe-145">상속자</span><span class="sxs-lookup"><span data-stu-id="a79fe-145">NOTES</span></span>

## <span data-ttu-id="a79fe-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a79fe-146">RELATED LINKS</span></span>
