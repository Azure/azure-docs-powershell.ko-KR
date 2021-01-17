---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/remove-azpeeringregisteredasn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Remove-AzPeeringRegisteredAsn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Remove-AzPeeringRegisteredAsn.md
ms.openlocfilehash: d43fe033b58ba6295728bc0c21ddb1d853587b59
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98330825"
---
# <span data-ttu-id="c319c-101">Remove-AzPeeringRegisteredAsn</span><span class="sxs-lookup"><span data-stu-id="c319c-101">Remove-AzPeeringRegisteredAsn</span></span>

## <span data-ttu-id="c319c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c319c-102">SYNOPSIS</span></span>
<span data-ttu-id="c319c-103">부모 피어링 리소스에서 등록된 ASN을 삭제하거나 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="c319c-103">Delete or remove a registered ASN from the parent peering resource.</span></span>

## <span data-ttu-id="c319c-104">구문</span><span class="sxs-lookup"><span data-stu-id="c319c-104">SYNTAX</span></span>

### <span data-ttu-id="c319c-105">ByName(기본값)</span><span class="sxs-lookup"><span data-stu-id="c319c-105">ByName (Default)</span></span>
```
Remove-AzPeeringRegisteredAsn [-ResourceGroupName] <String> [-PeeringName] <String> [-Name] <String> [-Force]
 [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c319c-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="c319c-106">InputObject</span></span>
```
Remove-AzPeeringRegisteredAsn -InputObject <PSPeeringServicePrefix> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c319c-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="c319c-107">ByResourceId</span></span>
```
Remove-AzPeeringRegisteredAsn [-ResourceId] <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c319c-108">설명</span><span class="sxs-lookup"><span data-stu-id="c319c-108">DESCRIPTION</span></span>
<span data-ttu-id="c319c-109">부모 피어링 리소스에서 등록된 ASN을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="c319c-109">Allows the removal of registered ASN from parent peering resource.</span></span>

## <span data-ttu-id="c319c-110">예제</span><span class="sxs-lookup"><span data-stu-id="c319c-110">EXAMPLES</span></span>

### <span data-ttu-id="c319c-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="c319c-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzPeeringRegisteredAsn -ResourceId $resourceId
```

<span data-ttu-id="c319c-112">리소스 ID로 등록된 ASN을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="c319c-112">Remove a registerd ASN by resource id.</span></span>

## <span data-ttu-id="c319c-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c319c-113">PARAMETERS</span></span>

### <span data-ttu-id="c319c-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c319c-114">-AsJob</span></span>
<span data-ttu-id="c319c-115">백그라운드에서 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="c319c-115">Run in the background.</span></span>

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

### <span data-ttu-id="c319c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c319c-116">-DefaultProfile</span></span>
<span data-ttu-id="c319c-117">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c319c-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c319c-118">-Force</span><span class="sxs-lookup"><span data-stu-id="c319c-118">-Force</span></span>
<span data-ttu-id="c319c-119">작업을 강제로 완료합니다.</span><span class="sxs-lookup"><span data-stu-id="c319c-119">Force the operation to complete</span></span>

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

### <span data-ttu-id="c319c-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c319c-120">-InputObject</span></span>
<span data-ttu-id="c319c-121">다음 Get-AzPeeringServicePrefix</span><span class="sxs-lookup"><span data-stu-id="c319c-121">Use a Get-AzPeeringServicePrefix</span></span>

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

### <span data-ttu-id="c319c-122">-Name</span><span class="sxs-lookup"><span data-stu-id="c319c-122">-Name</span></span>
<span data-ttu-id="c319c-123">등록된 ASN의 이름</span><span class="sxs-lookup"><span data-stu-id="c319c-123">The name of the registered ASN</span></span>

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

### <span data-ttu-id="c319c-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c319c-124">-PassThru</span></span>
<span data-ttu-id="c319c-125">{{ PassThru 설명 채우기 }}</span><span class="sxs-lookup"><span data-stu-id="c319c-125">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="c319c-126">-PeeringName</span><span class="sxs-lookup"><span data-stu-id="c319c-126">-PeeringName</span></span>
<span data-ttu-id="c319c-127">PSPeering의 고유 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c319c-127">The unique name of the PSPeering.</span></span>

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

### <span data-ttu-id="c319c-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c319c-128">-ResourceGroupName</span></span>
<span data-ttu-id="c319c-129">기존 리소스 그룹 이름을 만들거나 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="c319c-129">The create or use an existing resource group name.</span></span>

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

### <span data-ttu-id="c319c-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c319c-130">-ResourceId</span></span>
<span data-ttu-id="c319c-131">리소스 ID 문자열 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c319c-131">The resource id string name.</span></span>

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

### <span data-ttu-id="c319c-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c319c-132">-Confirm</span></span>
<span data-ttu-id="c319c-133">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="c319c-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c319c-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c319c-134">-WhatIf</span></span>
<span data-ttu-id="c319c-135">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="c319c-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c319c-136">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c319c-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c319c-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c319c-137">CommonParameters</span></span>
<span data-ttu-id="c319c-138">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="c319c-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c319c-139">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="c319c-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c319c-140">입력</span><span class="sxs-lookup"><span data-stu-id="c319c-140">INPUTS</span></span>

### <span data-ttu-id="c319c-141">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringServicePrefix</span><span class="sxs-lookup"><span data-stu-id="c319c-141">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringServicePrefix</span></span>

### <span data-ttu-id="c319c-142">System.String</span><span class="sxs-lookup"><span data-stu-id="c319c-142">System.String</span></span>

## <span data-ttu-id="c319c-143">출력</span><span class="sxs-lookup"><span data-stu-id="c319c-143">OUTPUTS</span></span>

### <span data-ttu-id="c319c-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="c319c-144">System.Boolean</span></span>

## <span data-ttu-id="c319c-145">참고 사항</span><span class="sxs-lookup"><span data-stu-id="c319c-145">NOTES</span></span>

## <span data-ttu-id="c319c-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c319c-146">RELATED LINKS</span></span>
