---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/remove-azpeeringregisteredprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Remove-AzPeeringRegisteredPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Remove-AzPeeringRegisteredPrefix.md
ms.openlocfilehash: b3d505d7c9412b15c2933ec03bb66af6f43a6b26
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98372065"
---
# <span data-ttu-id="e7a6a-101">Remove-AzPeeringRegisteredPrefix</span><span class="sxs-lookup"><span data-stu-id="e7a6a-101">Remove-AzPeeringRegisteredPrefix</span></span>

## <span data-ttu-id="e7a6a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e7a6a-102">SYNOPSIS</span></span>
<span data-ttu-id="e7a6a-103">부모 피어링 리소스에서 등록된 prefix를 삭제하거나 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="e7a6a-103">Delete or remove a registered prefix from the parent peering resource.</span></span>

## <span data-ttu-id="e7a6a-104">구문</span><span class="sxs-lookup"><span data-stu-id="e7a6a-104">SYNTAX</span></span>

### <span data-ttu-id="e7a6a-105">ByName(기본값)</span><span class="sxs-lookup"><span data-stu-id="e7a6a-105">ByName (Default)</span></span>
```
Remove-AzPeeringRegisteredPrefix [-ResourceGroupName] <String> [-PeeringName] <String> [-Name] <String>
 [-Force] [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e7a6a-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="e7a6a-106">InputObject</span></span>
```
Remove-AzPeeringRegisteredPrefix -InputObject <PSPeeringServicePrefix> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e7a6a-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="e7a6a-107">ByResourceId</span></span>
```
Remove-AzPeeringRegisteredPrefix [-ResourceId] <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e7a6a-108">설명</span><span class="sxs-lookup"><span data-stu-id="e7a6a-108">DESCRIPTION</span></span>
<span data-ttu-id="e7a6a-109">부모 피어링 리소스에서 등록된 사전 제거를 허용합니다.</span><span class="sxs-lookup"><span data-stu-id="e7a6a-109">Allows the removal of registered prefix from parent peering resource.</span></span>

## <span data-ttu-id="e7a6a-110">예제</span><span class="sxs-lookup"><span data-stu-id="e7a6a-110">EXAMPLES</span></span>

### <span data-ttu-id="e7a6a-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="e7a6a-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzPeeringRegisteredPrefix -ResourceId $resourceId
```

<span data-ttu-id="e7a6a-112">리소스 ID로 등록된 연결기를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="e7a6a-112">Remove a registerd prefix by resource id.</span></span>

## <span data-ttu-id="e7a6a-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e7a6a-113">PARAMETERS</span></span>

### <span data-ttu-id="e7a6a-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e7a6a-114">-AsJob</span></span>
<span data-ttu-id="e7a6a-115">백그라운드에서 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="e7a6a-115">Run in the background.</span></span>

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

### <span data-ttu-id="e7a6a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e7a6a-116">-DefaultProfile</span></span>
<span data-ttu-id="e7a6a-117">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e7a6a-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e7a6a-118">-Force</span><span class="sxs-lookup"><span data-stu-id="e7a6a-118">-Force</span></span>
<span data-ttu-id="e7a6a-119">작업을 강제로 완료합니다.</span><span class="sxs-lookup"><span data-stu-id="e7a6a-119">Force the operation to complete</span></span>

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

### <span data-ttu-id="e7a6a-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e7a6a-120">-InputObject</span></span>
<span data-ttu-id="e7a6a-121">다음 Get-AzPeering</span><span class="sxs-lookup"><span data-stu-id="e7a6a-121">Use a Get-AzPeering</span></span>

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

### <span data-ttu-id="e7a6a-122">-Name</span><span class="sxs-lookup"><span data-stu-id="e7a6a-122">-Name</span></span>
<span data-ttu-id="e7a6a-123">prefix의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e7a6a-123">The name of prefix.</span></span>

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

### <span data-ttu-id="e7a6a-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e7a6a-124">-PassThru</span></span>
<span data-ttu-id="e7a6a-125">{{ PassThru 설명 채우기 }}</span><span class="sxs-lookup"><span data-stu-id="e7a6a-125">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="e7a6a-126">-PeeringName</span><span class="sxs-lookup"><span data-stu-id="e7a6a-126">-PeeringName</span></span>
<span data-ttu-id="e7a6a-127">PSPeering의 고유 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e7a6a-127">The unique name of the PSPeering.</span></span>

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

### <span data-ttu-id="e7a6a-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e7a6a-128">-ResourceGroupName</span></span>
<span data-ttu-id="e7a6a-129">기존 리소스 그룹 이름을 만들거나 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="e7a6a-129">The create or use an existing resource group name.</span></span>

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

### <span data-ttu-id="e7a6a-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e7a6a-130">-ResourceId</span></span>
<span data-ttu-id="e7a6a-131">리소스 ID 문자열 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e7a6a-131">The resource id string name.</span></span>

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

### <span data-ttu-id="e7a6a-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e7a6a-132">-Confirm</span></span>
<span data-ttu-id="e7a6a-133">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="e7a6a-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e7a6a-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e7a6a-134">-WhatIf</span></span>
<span data-ttu-id="e7a6a-135">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="e7a6a-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e7a6a-136">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e7a6a-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e7a6a-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7a6a-137">CommonParameters</span></span>
<span data-ttu-id="e7a6a-138">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="e7a6a-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7a6a-139">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="e7a6a-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7a6a-140">입력</span><span class="sxs-lookup"><span data-stu-id="e7a6a-140">INPUTS</span></span>

### <span data-ttu-id="e7a6a-141">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringServicePrefix</span><span class="sxs-lookup"><span data-stu-id="e7a6a-141">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringServicePrefix</span></span>

### <span data-ttu-id="e7a6a-142">System.String</span><span class="sxs-lookup"><span data-stu-id="e7a6a-142">System.String</span></span>

## <span data-ttu-id="e7a6a-143">출력</span><span class="sxs-lookup"><span data-stu-id="e7a6a-143">OUTPUTS</span></span>

### <span data-ttu-id="e7a6a-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="e7a6a-144">System.Boolean</span></span>

## <span data-ttu-id="e7a6a-145">참고 사항</span><span class="sxs-lookup"><span data-stu-id="e7a6a-145">NOTES</span></span>

## <span data-ttu-id="e7a6a-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e7a6a-146">RELATED LINKS</span></span>
