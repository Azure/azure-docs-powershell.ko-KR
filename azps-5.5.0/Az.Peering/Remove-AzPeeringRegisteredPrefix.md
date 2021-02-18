---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/remove-azpeeringregisteredprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Remove-AzPeeringRegisteredPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Remove-AzPeeringRegisteredPrefix.md
ms.openlocfilehash: b3d505d7c9412b15c2933ec03bb66af6f43a6b26
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100206280"
---
# <span data-ttu-id="7e2ab-101">Remove-AzPeeringRegisteredPrefix</span><span class="sxs-lookup"><span data-stu-id="7e2ab-101">Remove-AzPeeringRegisteredPrefix</span></span>

## <span data-ttu-id="7e2ab-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7e2ab-102">SYNOPSIS</span></span>
<span data-ttu-id="7e2ab-103">부모 피어링 리소스에서 등록된 prefix를 삭제하거나 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="7e2ab-103">Delete or remove a registered prefix from the parent peering resource.</span></span>

## <span data-ttu-id="7e2ab-104">구문</span><span class="sxs-lookup"><span data-stu-id="7e2ab-104">SYNTAX</span></span>

### <span data-ttu-id="7e2ab-105">ByName(기본값)</span><span class="sxs-lookup"><span data-stu-id="7e2ab-105">ByName (Default)</span></span>
```
Remove-AzPeeringRegisteredPrefix [-ResourceGroupName] <String> [-PeeringName] <String> [-Name] <String>
 [-Force] [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7e2ab-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="7e2ab-106">InputObject</span></span>
```
Remove-AzPeeringRegisteredPrefix -InputObject <PSPeeringServicePrefix> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7e2ab-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="7e2ab-107">ByResourceId</span></span>
```
Remove-AzPeeringRegisteredPrefix [-ResourceId] <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7e2ab-108">설명</span><span class="sxs-lookup"><span data-stu-id="7e2ab-108">DESCRIPTION</span></span>
<span data-ttu-id="7e2ab-109">부모 피어링 리소스에서 등록된 연결의 제거를 허용합니다.</span><span class="sxs-lookup"><span data-stu-id="7e2ab-109">Allows the removal of registered prefix from parent peering resource.</span></span>

## <span data-ttu-id="7e2ab-110">예제</span><span class="sxs-lookup"><span data-stu-id="7e2ab-110">EXAMPLES</span></span>

### <span data-ttu-id="7e2ab-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="7e2ab-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzPeeringRegisteredPrefix -ResourceId $resourceId
```

<span data-ttu-id="7e2ab-112">리소스 ID로 등록된 연결기를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="7e2ab-112">Remove a registerd prefix by resource id.</span></span>

## <span data-ttu-id="7e2ab-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7e2ab-113">PARAMETERS</span></span>

### <span data-ttu-id="7e2ab-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7e2ab-114">-AsJob</span></span>
<span data-ttu-id="7e2ab-115">백그라운드에서 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="7e2ab-115">Run in the background.</span></span>

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

### <span data-ttu-id="7e2ab-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e2ab-116">-DefaultProfile</span></span>
<span data-ttu-id="7e2ab-117">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7e2ab-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7e2ab-118">-Force</span><span class="sxs-lookup"><span data-stu-id="7e2ab-118">-Force</span></span>
<span data-ttu-id="7e2ab-119">작업을 강제로 완료합니다.</span><span class="sxs-lookup"><span data-stu-id="7e2ab-119">Force the operation to complete</span></span>

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

### <span data-ttu-id="7e2ab-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7e2ab-120">-InputObject</span></span>
<span data-ttu-id="7e2ab-121">다음 Get-AzPeering</span><span class="sxs-lookup"><span data-stu-id="7e2ab-121">Use a Get-AzPeering</span></span>

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

### <span data-ttu-id="7e2ab-122">-Name</span><span class="sxs-lookup"><span data-stu-id="7e2ab-122">-Name</span></span>
<span data-ttu-id="7e2ab-123">prefix의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7e2ab-123">The name of prefix.</span></span>

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

### <span data-ttu-id="7e2ab-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7e2ab-124">-PassThru</span></span>
<span data-ttu-id="7e2ab-125">{{ PassThru 설명 채우기 }}</span><span class="sxs-lookup"><span data-stu-id="7e2ab-125">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="7e2ab-126">-PeeringName</span><span class="sxs-lookup"><span data-stu-id="7e2ab-126">-PeeringName</span></span>
<span data-ttu-id="7e2ab-127">PSPeering의 고유 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7e2ab-127">The unique name of the PSPeering.</span></span>

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

### <span data-ttu-id="7e2ab-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7e2ab-128">-ResourceGroupName</span></span>
<span data-ttu-id="7e2ab-129">기존 리소스 그룹 이름을 만들거나 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e2ab-129">The create or use an existing resource group name.</span></span>

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

### <span data-ttu-id="7e2ab-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7e2ab-130">-ResourceId</span></span>
<span data-ttu-id="7e2ab-131">리소스 ID 문자열 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7e2ab-131">The resource id string name.</span></span>

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

### <span data-ttu-id="7e2ab-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7e2ab-132">-Confirm</span></span>
<span data-ttu-id="7e2ab-133">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="7e2ab-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7e2ab-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7e2ab-134">-WhatIf</span></span>
<span data-ttu-id="7e2ab-135">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="7e2ab-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7e2ab-136">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7e2ab-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7e2ab-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e2ab-137">CommonParameters</span></span>
<span data-ttu-id="7e2ab-138">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="7e2ab-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e2ab-139">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="7e2ab-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e2ab-140">입력</span><span class="sxs-lookup"><span data-stu-id="7e2ab-140">INPUTS</span></span>

### <span data-ttu-id="7e2ab-141">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringServicePrefix</span><span class="sxs-lookup"><span data-stu-id="7e2ab-141">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringServicePrefix</span></span>

### <span data-ttu-id="7e2ab-142">System.String</span><span class="sxs-lookup"><span data-stu-id="7e2ab-142">System.String</span></span>

## <span data-ttu-id="7e2ab-143">출력</span><span class="sxs-lookup"><span data-stu-id="7e2ab-143">OUTPUTS</span></span>

### <span data-ttu-id="7e2ab-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="7e2ab-144">System.Boolean</span></span>

## <span data-ttu-id="7e2ab-145">참고 사항</span><span class="sxs-lookup"><span data-stu-id="7e2ab-145">NOTES</span></span>

## <span data-ttu-id="7e2ab-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7e2ab-146">RELATED LINKS</span></span>
