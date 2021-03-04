---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 60BED40A-EEA4-4667-93E9-8A9B35037726
online version: https://docs.microsoft.com/powershell/module/az.resources/move-azresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Move-AzResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Move-AzResource.md
ms.openlocfilehash: 16e43df2da9509d7fb222f3299a4c611d146026c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101962656"
---
# <span data-ttu-id="6688d-101">Move-AzResource</span><span class="sxs-lookup"><span data-stu-id="6688d-101">Move-AzResource</span></span>

## <span data-ttu-id="6688d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6688d-102">SYNOPSIS</span></span>
<span data-ttu-id="6688d-103">리소스를 다른 리소스 그룹 또는 구독으로 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="6688d-103">Moves a resource to a different resource group or subscription.</span></span>

## <span data-ttu-id="6688d-104">구문</span><span class="sxs-lookup"><span data-stu-id="6688d-104">SYNTAX</span></span>

```
Move-AzResource -DestinationResourceGroupName <String> [-DestinationSubscriptionId <Guid>]
 -ResourceId <String[]> [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6688d-105">설명</span><span class="sxs-lookup"><span data-stu-id="6688d-105">DESCRIPTION</span></span>
<span data-ttu-id="6688d-106">**Move-AzResource** cmdlet은 기존 리소스를 다른 리소스 그룹으로 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="6688d-106">The **Move-AzResource** cmdlet moves existing resources to a different resource group.</span></span>
<span data-ttu-id="6688d-107">이 리소스 그룹은 다른 구독에 있을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6688d-107">That resource group can be in a different subscription.</span></span>

## <span data-ttu-id="6688d-108">예제</span><span class="sxs-lookup"><span data-stu-id="6688d-108">EXAMPLES</span></span>

### <span data-ttu-id="6688d-109">예제 1: 리소스 그룹으로 리소스 이동</span><span class="sxs-lookup"><span data-stu-id="6688d-109">Example 1: Move a resource to a resource group</span></span>
```
PS C:\>$Resource = Get-AzResource -ResourceType "Microsoft.ClassicCompute/storageAccounts" -ResourceName "ContosoStorageAccount"
PS C:\> Move-AzResource -ResourceId $Resource.ResourceId -DestinationResourceGroupName "ResourceGroup14"
```

<span data-ttu-id="6688d-110">첫 번째 명령은 contosoStorageAccount라는 리소스를 Get-AzResource cmdlet을 사용한 다음 해당 $Resource 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="6688d-110">The first command gets a resource named ContosoStorageAccount by using the Get-AzResource cmdlet, and then stores that resource in the $Resource variable.</span></span>
<span data-ttu-id="6688d-111">두 번째 명령은 리소스 그룹인 ResourceGroup14로 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="6688d-111">The second command moves that resource into the resource group named ResourceGroup14.</span></span>
<span data-ttu-id="6688d-112">명령은 리소스의 **ResourceId** 속성을 사용하여 이동할 리소스를 $Resource.</span><span class="sxs-lookup"><span data-stu-id="6688d-112">The command identifies the resource to move by using the **ResourceId** property of $Resource.</span></span>

## <span data-ttu-id="6688d-113">매개 변수</span><span class="sxs-lookup"><span data-stu-id="6688d-113">PARAMETERS</span></span>

### <span data-ttu-id="6688d-114">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="6688d-114">-ApiVersion</span></span>
<span data-ttu-id="6688d-115">사용할 리소스 공급자 API의 버전을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="6688d-115">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="6688d-116">버전을 지정하지 않으면 이 cmdlet에서는 사용 가능한 최신 버전을 사용하게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6688d-116">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="6688d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6688d-117">-DefaultProfile</span></span>
<span data-ttu-id="6688d-118">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="6688d-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6688d-119">-DestinationResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6688d-119">-DestinationResourceGroupName</span></span>
<span data-ttu-id="6688d-120">이 cmdlet이 리소스를 이동하는 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="6688d-120">Specifies the name of the resource group into which this cmdlet moves resources.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: TargetResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6688d-121">-DestinationSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="6688d-121">-DestinationSubscriptionId</span></span>
<span data-ttu-id="6688d-122">이 cmdlet이 리소스를 이동하는 구독의 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="6688d-122">Specifies the ID of the subscription into which this cmdlet moves resources .</span></span>

```yaml
Type: System.Nullable`1[System.Guid]
Parameter Sets: (All)
Aliases: Id, SubscriptionId

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6688d-123">-Force</span><span class="sxs-lookup"><span data-stu-id="6688d-123">-Force</span></span>
<span data-ttu-id="6688d-124">사용자 확인을 요청하지 않고 명령을 강제로 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="6688d-124">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="6688d-125">-Pre</span><span class="sxs-lookup"><span data-stu-id="6688d-125">-Pre</span></span>
<span data-ttu-id="6688d-126">이 cmdlet은 사용할 버전을 자동으로 결정할 때 릴리스 전 API 버전을 고려하고 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6688d-126">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="6688d-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6688d-127">-ResourceId</span></span>
<span data-ttu-id="6688d-128">이 cmdlet이 이동하는 리소스의 아이디 배열을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="6688d-128">Specifies an array of IDs of the resources that this cmdlet moves.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6688d-129">-확인</span><span class="sxs-lookup"><span data-stu-id="6688d-129">-Confirm</span></span>
<span data-ttu-id="6688d-130">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="6688d-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6688d-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6688d-131">-WhatIf</span></span>
<span data-ttu-id="6688d-132">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="6688d-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6688d-133">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6688d-133">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6688d-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6688d-134">CommonParameters</span></span>
<span data-ttu-id="6688d-135">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="6688d-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6688d-136">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6688d-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6688d-137">입력</span><span class="sxs-lookup"><span data-stu-id="6688d-137">INPUTS</span></span>

### <span data-ttu-id="6688d-138">System.Nullable'1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="6688d-138">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="6688d-139">System.String[]</span><span class="sxs-lookup"><span data-stu-id="6688d-139">System.String[]</span></span>

## <span data-ttu-id="6688d-140">출력</span><span class="sxs-lookup"><span data-stu-id="6688d-140">OUTPUTS</span></span>

### <span data-ttu-id="6688d-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="6688d-141">System.Boolean</span></span>

## <span data-ttu-id="6688d-142">참고 사항</span><span class="sxs-lookup"><span data-stu-id="6688d-142">NOTES</span></span>

## <span data-ttu-id="6688d-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6688d-143">RELATED LINKS</span></span>

[<span data-ttu-id="6688d-144">Get-AzResource</span><span class="sxs-lookup"><span data-stu-id="6688d-144">Get-AzResource</span></span>](./Get-AzResource.md)

[<span data-ttu-id="6688d-145">New-AzResource</span><span class="sxs-lookup"><span data-stu-id="6688d-145">New-AzResource</span></span>](./New-AzResource.md)

[<span data-ttu-id="6688d-146">Remove-AzResource</span><span class="sxs-lookup"><span data-stu-id="6688d-146">Remove-AzResource</span></span>](./Remove-AzResource.md)

[<span data-ttu-id="6688d-147">Set-AzResource</span><span class="sxs-lookup"><span data-stu-id="6688d-147">Set-AzResource</span></span>](./Set-AzResource.md)


