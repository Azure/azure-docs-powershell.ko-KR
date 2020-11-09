---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/remove-azpeeringregisteredprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Remove-AzPeeringRegisteredPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Remove-AzPeeringRegisteredPrefix.md
ms.openlocfilehash: b3d505d7c9412b15c2933ec03bb66af6f43a6b26
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94310142"
---
# <span data-ttu-id="be4b6-101">Remove-AzPeeringRegisteredPrefix</span><span class="sxs-lookup"><span data-stu-id="be4b6-101">Remove-AzPeeringRegisteredPrefix</span></span>

## <span data-ttu-id="be4b6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="be4b6-102">SYNOPSIS</span></span>
<span data-ttu-id="be4b6-103">부모 피어 링 리소스에서 등록 된 접두사를 삭제 하거나 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="be4b6-103">Delete or remove a registered prefix from the parent peering resource.</span></span>

## <span data-ttu-id="be4b6-104">구문과</span><span class="sxs-lookup"><span data-stu-id="be4b6-104">SYNTAX</span></span>

### <span data-ttu-id="be4b6-105">ByName (기본값)</span><span class="sxs-lookup"><span data-stu-id="be4b6-105">ByName (Default)</span></span>
```
Remove-AzPeeringRegisteredPrefix [-ResourceGroupName] <String> [-PeeringName] <String> [-Name] <String>
 [-Force] [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="be4b6-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="be4b6-106">InputObject</span></span>
```
Remove-AzPeeringRegisteredPrefix -InputObject <PSPeeringServicePrefix> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="be4b6-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="be4b6-107">ByResourceId</span></span>
```
Remove-AzPeeringRegisteredPrefix [-ResourceId] <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="be4b6-108">설명은</span><span class="sxs-lookup"><span data-stu-id="be4b6-108">DESCRIPTION</span></span>
<span data-ttu-id="be4b6-109">부모 피어 링 리소스에서 등록 된 접두사를 제거할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="be4b6-109">Allows the removal of registered prefix from parent peering resource.</span></span>

## <span data-ttu-id="be4b6-110">예제의</span><span class="sxs-lookup"><span data-stu-id="be4b6-110">EXAMPLES</span></span>

### <span data-ttu-id="be4b6-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="be4b6-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzPeeringRegisteredPrefix -ResourceId $resourceId
```

<span data-ttu-id="be4b6-112">리소스 id를 기준으로 registerd 접두사를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="be4b6-112">Remove a registerd prefix by resource id.</span></span>

## <span data-ttu-id="be4b6-113">변수</span><span class="sxs-lookup"><span data-stu-id="be4b6-113">PARAMETERS</span></span>

### <span data-ttu-id="be4b6-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="be4b6-114">-AsJob</span></span>
<span data-ttu-id="be4b6-115">백그라운드에서 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="be4b6-115">Run in the background.</span></span>

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

### <span data-ttu-id="be4b6-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="be4b6-116">-DefaultProfile</span></span>
<span data-ttu-id="be4b6-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="be4b6-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="be4b6-118">-Force</span><span class="sxs-lookup"><span data-stu-id="be4b6-118">-Force</span></span>
<span data-ttu-id="be4b6-119">강제로 작업 완료</span><span class="sxs-lookup"><span data-stu-id="be4b6-119">Force the operation to complete</span></span>

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

### <span data-ttu-id="be4b6-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="be4b6-120">-InputObject</span></span>
<span data-ttu-id="be4b6-121">Get-AzPeering 사용</span><span class="sxs-lookup"><span data-stu-id="be4b6-121">Use a Get-AzPeering</span></span>

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

### <span data-ttu-id="be4b6-122">-이름</span><span class="sxs-lookup"><span data-stu-id="be4b6-122">-Name</span></span>
<span data-ttu-id="be4b6-123">접두사의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="be4b6-123">The name of prefix.</span></span>

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

### <span data-ttu-id="be4b6-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="be4b6-124">-PassThru</span></span>
<span data-ttu-id="be4b6-125">{{Fill PassThru 설명}}</span><span class="sxs-lookup"><span data-stu-id="be4b6-125">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="be4b6-126">-PeeringName</span><span class="sxs-lookup"><span data-stu-id="be4b6-126">-PeeringName</span></span>
<span data-ttu-id="be4b6-127">PSPeering의 고유 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="be4b6-127">The unique name of the PSPeering.</span></span>

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

### <span data-ttu-id="be4b6-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="be4b6-128">-ResourceGroupName</span></span>
<span data-ttu-id="be4b6-129">기존 리소스 그룹 이름을 만들거나 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="be4b6-129">The create or use an existing resource group name.</span></span>

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

### <span data-ttu-id="be4b6-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="be4b6-130">-ResourceId</span></span>
<span data-ttu-id="be4b6-131">리소스 id 문자열 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="be4b6-131">The resource id string name.</span></span>

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

### <span data-ttu-id="be4b6-132">-확인</span><span class="sxs-lookup"><span data-stu-id="be4b6-132">-Confirm</span></span>
<span data-ttu-id="be4b6-133">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="be4b6-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="be4b6-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="be4b6-134">-WhatIf</span></span>
<span data-ttu-id="be4b6-135">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="be4b6-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="be4b6-136">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="be4b6-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="be4b6-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="be4b6-137">CommonParameters</span></span>
<span data-ttu-id="be4b6-138">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="be4b6-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="be4b6-139">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="be4b6-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="be4b6-140">입력</span><span class="sxs-lookup"><span data-stu-id="be4b6-140">INPUTS</span></span>

### <span data-ttu-id="be4b6-141">PSPeeringServicePrefix (Microsoft. PowerShell.</span><span class="sxs-lookup"><span data-stu-id="be4b6-141">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringServicePrefix</span></span>

### <span data-ttu-id="be4b6-142">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="be4b6-142">System.String</span></span>

## <span data-ttu-id="be4b6-143">출력</span><span class="sxs-lookup"><span data-stu-id="be4b6-143">OUTPUTS</span></span>

### <span data-ttu-id="be4b6-144">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="be4b6-144">System.Boolean</span></span>

## <span data-ttu-id="be4b6-145">상속자</span><span class="sxs-lookup"><span data-stu-id="be4b6-145">NOTES</span></span>

## <span data-ttu-id="be4b6-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="be4b6-146">RELATED LINKS</span></span>
