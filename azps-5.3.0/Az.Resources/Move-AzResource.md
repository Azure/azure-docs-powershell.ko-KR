---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 60BED40A-EEA4-4667-93E9-8A9B35037726
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/move-azresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Move-AzResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Move-AzResource.md
ms.openlocfilehash: d14d591ffdc0e20934a0cf758407dc2b4e6e152c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98490448"
---
# <span data-ttu-id="0d7cb-101">Move-AzResource</span><span class="sxs-lookup"><span data-stu-id="0d7cb-101">Move-AzResource</span></span>

## <span data-ttu-id="0d7cb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0d7cb-102">SYNOPSIS</span></span>
<span data-ttu-id="0d7cb-103">리소스를 다른 리소스 그룹 또는 구독으로 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="0d7cb-103">Moves a resource to a different resource group or subscription.</span></span>

## <span data-ttu-id="0d7cb-104">구문</span><span class="sxs-lookup"><span data-stu-id="0d7cb-104">SYNTAX</span></span>

```
Move-AzResource -DestinationResourceGroupName <String> [-DestinationSubscriptionId <Guid>]
 -ResourceId <String[]> [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0d7cb-105">설명</span><span class="sxs-lookup"><span data-stu-id="0d7cb-105">DESCRIPTION</span></span>
<span data-ttu-id="0d7cb-106">**Move-AzResource** cmdlet은 기존 리소스를 다른 리소스 그룹으로 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="0d7cb-106">The **Move-AzResource** cmdlet moves existing resources to a different resource group.</span></span>
<span data-ttu-id="0d7cb-107">이 리소스 그룹은 다른 구독에 있을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0d7cb-107">That resource group can be in a different subscription.</span></span>

## <span data-ttu-id="0d7cb-108">예제</span><span class="sxs-lookup"><span data-stu-id="0d7cb-108">EXAMPLES</span></span>

### <span data-ttu-id="0d7cb-109">예제 1: 리소스 그룹으로 리소스 이동</span><span class="sxs-lookup"><span data-stu-id="0d7cb-109">Example 1: Move a resource to a resource group</span></span>
```
PS C:\>$Resource = Get-AzResource -ResourceType "Microsoft.ClassicCompute/storageAccounts" -ResourceName "ContosoStorageAccount"
PS C:\> Move-AzResource -ResourceId $Resource.ResourceId -DestinationResourceGroupName "ResourceGroup14"
```

<span data-ttu-id="0d7cb-110">첫 번째 명령은 Get-AzResource cmdlet을 사용하여 ContosoStorageAccount라는 리소스를 $Resource 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="0d7cb-110">The first command gets a resource named ContosoStorageAccount by using the Get-AzResource cmdlet, and then stores that resource in the $Resource variable.</span></span>
<span data-ttu-id="0d7cb-111">두 번째 명령은 리소스 그룹을 ResourceGroup14로 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="0d7cb-111">The second command moves that resource into the resource group named ResourceGroup14.</span></span>
<span data-ttu-id="0d7cb-112">이 명령은 리소스의 **ResourceId** 속성을 사용하여 이동할 리소스를 $Resource.</span><span class="sxs-lookup"><span data-stu-id="0d7cb-112">The command identifies the resource to move by using the **ResourceId** property of $Resource.</span></span>

## <span data-ttu-id="0d7cb-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0d7cb-113">PARAMETERS</span></span>

### <span data-ttu-id="0d7cb-114">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="0d7cb-114">-ApiVersion</span></span>
<span data-ttu-id="0d7cb-115">사용할 리소스 공급자 API의 버전을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="0d7cb-115">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="0d7cb-116">버전을 지정하지 않으면 이 cmdlet은 사용 가능한 최신 버전을 사용하게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="0d7cb-116">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="0d7cb-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d7cb-117">-DefaultProfile</span></span>
<span data-ttu-id="0d7cb-118">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="0d7cb-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0d7cb-119">-DestinationResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0d7cb-119">-DestinationResourceGroupName</span></span>
<span data-ttu-id="0d7cb-120">이 cmdlet이 리소스를 이동하는 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="0d7cb-120">Specifies the name of the resource group into which this cmdlet moves resources.</span></span>

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

### <span data-ttu-id="0d7cb-121">-DestinationSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="0d7cb-121">-DestinationSubscriptionId</span></span>
<span data-ttu-id="0d7cb-122">이 cmdlet이 리소스를 이동하는 구독의 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="0d7cb-122">Specifies the ID of the subscription into which this cmdlet moves resources .</span></span>

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

### <span data-ttu-id="0d7cb-123">-Force</span><span class="sxs-lookup"><span data-stu-id="0d7cb-123">-Force</span></span>
<span data-ttu-id="0d7cb-124">사용자 확인을 요청하지 않고 명령을 강제로 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="0d7cb-124">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="0d7cb-125">-Pre</span><span class="sxs-lookup"><span data-stu-id="0d7cb-125">-Pre</span></span>
<span data-ttu-id="0d7cb-126">이 cmdlet은 사용할 버전을 자동으로 결정할 때 릴리스 전 API 버전을 고려합니다.</span><span class="sxs-lookup"><span data-stu-id="0d7cb-126">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="0d7cb-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0d7cb-127">-ResourceId</span></span>
<span data-ttu-id="0d7cb-128">이 cmdlet이 이동하는 리소스의 ID 배열을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="0d7cb-128">Specifies an array of IDs of the resources that this cmdlet moves.</span></span>

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

### <span data-ttu-id="0d7cb-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0d7cb-129">-Confirm</span></span>
<span data-ttu-id="0d7cb-130">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="0d7cb-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0d7cb-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0d7cb-131">-WhatIf</span></span>
<span data-ttu-id="0d7cb-132">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="0d7cb-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0d7cb-133">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0d7cb-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0d7cb-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d7cb-134">CommonParameters</span></span>
<span data-ttu-id="0d7cb-135">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="0d7cb-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d7cb-136">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="0d7cb-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d7cb-137">입력</span><span class="sxs-lookup"><span data-stu-id="0d7cb-137">INPUTS</span></span>

### <span data-ttu-id="0d7cb-138">System.Nullable'1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="0d7cb-138">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="0d7cb-139">System.String[]</span><span class="sxs-lookup"><span data-stu-id="0d7cb-139">System.String[]</span></span>

## <span data-ttu-id="0d7cb-140">출력</span><span class="sxs-lookup"><span data-stu-id="0d7cb-140">OUTPUTS</span></span>

### <span data-ttu-id="0d7cb-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="0d7cb-141">System.Boolean</span></span>

## <span data-ttu-id="0d7cb-142">참고 사항</span><span class="sxs-lookup"><span data-stu-id="0d7cb-142">NOTES</span></span>

## <span data-ttu-id="0d7cb-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0d7cb-143">RELATED LINKS</span></span>

[<span data-ttu-id="0d7cb-144">Get-AzResource</span><span class="sxs-lookup"><span data-stu-id="0d7cb-144">Get-AzResource</span></span>](./Get-AzResource.md)

[<span data-ttu-id="0d7cb-145">New-AzResource</span><span class="sxs-lookup"><span data-stu-id="0d7cb-145">New-AzResource</span></span>](./New-AzResource.md)

[<span data-ttu-id="0d7cb-146">Remove-AzResource</span><span class="sxs-lookup"><span data-stu-id="0d7cb-146">Remove-AzResource</span></span>](./Remove-AzResource.md)

[<span data-ttu-id="0d7cb-147">Set-AzResource</span><span class="sxs-lookup"><span data-stu-id="0d7cb-147">Set-AzResource</span></span>](./Set-AzResource.md)


