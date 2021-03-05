---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/powershell/module/az.peering/remove-azpeeringserviceprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Remove-AzPeeringServicePrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Remove-AzPeeringServicePrefix.md
ms.openlocfilehash: 3922492f4d72886e0608108811906387e31472b1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101989296"
---
# <span data-ttu-id="973eb-101">Remove-AzPeeringServicePrefix</span><span class="sxs-lookup"><span data-stu-id="973eb-101">Remove-AzPeeringServicePrefix</span></span>

## <span data-ttu-id="973eb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="973eb-102">SYNOPSIS</span></span>
<span data-ttu-id="973eb-103">새 피어링 서비스 연결선 제거</span><span class="sxs-lookup"><span data-stu-id="973eb-103">Removes a new peering service prefix</span></span>

## <span data-ttu-id="973eb-104">구문</span><span class="sxs-lookup"><span data-stu-id="973eb-104">SYNTAX</span></span>

### <span data-ttu-id="973eb-105">ByName(기본값)</span><span class="sxs-lookup"><span data-stu-id="973eb-105">ByName (Default)</span></span>
```
Remove-AzPeeringServicePrefix [-ResourceGroupName] <String> [-Name] <String> [-PrefixName] <String> [-Force]
 [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="973eb-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="973eb-106">InputObject</span></span>
```
Remove-AzPeeringServicePrefix [-InputObject] <PSPeeringServicePrefix> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="973eb-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="973eb-107">ByResourceId</span></span>
```
Remove-AzPeeringServicePrefix [-ResourceId] <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="973eb-108">설명</span><span class="sxs-lookup"><span data-stu-id="973eb-108">DESCRIPTION</span></span>
<span data-ttu-id="973eb-109">피어링 서비스에서 피어링 서비스 연결부를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="973eb-109">Removes a peering service prefix from a peering service.</span></span>

## <span data-ttu-id="973eb-110">예제</span><span class="sxs-lookup"><span data-stu-id="973eb-110">EXAMPLES</span></span>

### <span data-ttu-id="973eb-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="973eb-111">Example 1</span></span>
```powershell
PS C:\> Get-AzPeeringService -ResourceGroupName $rgName -Name $peeringServiceName | Remove-AzPeeringServicePrefix -Name $prefixName
```

<span data-ttu-id="973eb-112">피어링 서비스 개체에서 연결선 제거</span><span class="sxs-lookup"><span data-stu-id="973eb-112">Remove a prefix from a peering service object</span></span>

### <span data-ttu-id="973eb-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="973eb-113">Example 2</span></span>
```powershell
PS C:\> Remove-AzPeeringServicePrefix -ResourceId $peeringServiceResourceId -Name $prefixName -PassThru

True
```

<span data-ttu-id="973eb-114">피어링 서비스 리소스 ID에서 프레픽스를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="973eb-114">Remove a prefix from a peering service resource id.</span></span>

### <span data-ttu-id="973eb-115">예제 3</span><span class="sxs-lookup"><span data-stu-id="973eb-115">Example 3</span></span>
```powershell
PS C:\> Remove-AzPeeringServicePrefix -ResourceGroupName $peeringServiceGroup -PeeringServiceName $peeringServiceName -Name $prefixName -PassThru

True
```

<span data-ttu-id="973eb-116">피어링 서비스 리소스 그룹 이름 및 이름에서 연결선 제거</span><span class="sxs-lookup"><span data-stu-id="973eb-116">Remove a prefix from a peering service resource group name and name</span></span>

## <span data-ttu-id="973eb-117">매개 변수</span><span class="sxs-lookup"><span data-stu-id="973eb-117">PARAMETERS</span></span>

### <span data-ttu-id="973eb-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="973eb-118">-AsJob</span></span>
<span data-ttu-id="973eb-119">백그라운드에서 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="973eb-119">Run in the background.</span></span>

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

### <span data-ttu-id="973eb-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="973eb-120">-DefaultProfile</span></span>
<span data-ttu-id="973eb-121">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="973eb-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="973eb-122">-Force</span><span class="sxs-lookup"><span data-stu-id="973eb-122">-Force</span></span>
<span data-ttu-id="973eb-123">작업을 완료하기 위해 강제로</span><span class="sxs-lookup"><span data-stu-id="973eb-123">Force the operation to complete</span></span>

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

### <span data-ttu-id="973eb-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="973eb-124">-InputObject</span></span>
<span data-ttu-id="973eb-125">Get-AzPeeringServicePrefix</span><span class="sxs-lookup"><span data-stu-id="973eb-125">Use a Get-AzPeeringServicePrefix</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringServicePrefix
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="973eb-126">-Name</span><span class="sxs-lookup"><span data-stu-id="973eb-126">-Name</span></span>
<span data-ttu-id="973eb-127">PSPeering의 고유한 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="973eb-127">The unique name of the PSPeering.</span></span>

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

### <span data-ttu-id="973eb-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="973eb-128">-PassThru</span></span>
<span data-ttu-id="973eb-129">실패한 경우 성공 또는 false에 대해 true를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="973eb-129">Returns true for success or false for failed.</span></span>

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

### <span data-ttu-id="973eb-130">-PrefixName</span><span class="sxs-lookup"><span data-stu-id="973eb-130">-PrefixName</span></span>
<span data-ttu-id="973eb-131">도두사 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="973eb-131">The name of prefix.</span></span>

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

### <span data-ttu-id="973eb-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="973eb-132">-ResourceGroupName</span></span>
<span data-ttu-id="973eb-133">기존 리소스 그룹 이름을 만들거나 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="973eb-133">The create or use an existing resource group name.</span></span>

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

### <span data-ttu-id="973eb-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="973eb-134">-ResourceId</span></span>
<span data-ttu-id="973eb-135">리소스 ID 문자열 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="973eb-135">The resource id string name.</span></span>

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

### <span data-ttu-id="973eb-136">-확인</span><span class="sxs-lookup"><span data-stu-id="973eb-136">-Confirm</span></span>
<span data-ttu-id="973eb-137">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="973eb-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="973eb-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="973eb-138">-WhatIf</span></span>
<span data-ttu-id="973eb-139">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="973eb-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="973eb-140">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="973eb-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="973eb-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="973eb-141">CommonParameters</span></span>
<span data-ttu-id="973eb-142">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="973eb-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="973eb-143">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="973eb-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="973eb-144">입력</span><span class="sxs-lookup"><span data-stu-id="973eb-144">INPUTS</span></span>

### <span data-ttu-id="973eb-145">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringServicePrefix</span><span class="sxs-lookup"><span data-stu-id="973eb-145">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringServicePrefix</span></span>

### <span data-ttu-id="973eb-146">System.String</span><span class="sxs-lookup"><span data-stu-id="973eb-146">System.String</span></span>

## <span data-ttu-id="973eb-147">출력</span><span class="sxs-lookup"><span data-stu-id="973eb-147">OUTPUTS</span></span>

### <span data-ttu-id="973eb-148">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="973eb-148">System.Boolean</span></span>

## <span data-ttu-id="973eb-149">참고 사항</span><span class="sxs-lookup"><span data-stu-id="973eb-149">NOTES</span></span>

## <span data-ttu-id="973eb-150">관련 링크</span><span class="sxs-lookup"><span data-stu-id="973eb-150">RELATED LINKS</span></span>
