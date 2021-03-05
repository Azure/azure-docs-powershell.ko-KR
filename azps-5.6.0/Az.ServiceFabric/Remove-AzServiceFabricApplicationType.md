---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/powershell/module/az.servicefabric/remove-azservicefabricapplicationtype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricApplicationType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricApplicationType.md
ms.openlocfilehash: dbd2e29a3136576ecf5596c4a401d689fd0631a3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102005579"
---
# <span data-ttu-id="ef379-101">Remove-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="ef379-101">Remove-AzServiceFabricApplicationType</span></span>

## <span data-ttu-id="ef379-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ef379-102">SYNOPSIS</span></span>
<span data-ttu-id="ef379-103">클러스터에서 Service 패브릭 애플리케이션 유형을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="ef379-103">Remove Service fabric an application type from the cluster.</span></span> <span data-ttu-id="ef379-104">이렇게 하면 이 리소스의 모든 형식 버전이 제거됩니다.</span><span class="sxs-lookup"><span data-stu-id="ef379-104">This will remove all type versions under this resource.</span></span> <span data-ttu-id="ef379-105">배포된 ARM 형식만 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="ef379-105">Only supports ARM deployed application types.</span></span>

## <span data-ttu-id="ef379-106">구문</span><span class="sxs-lookup"><span data-stu-id="ef379-106">SYNTAX</span></span>

### <span data-ttu-id="ef379-107">ByResourceGroup(기본값)</span><span class="sxs-lookup"><span data-stu-id="ef379-107">ByResourceGroup (Default)</span></span>
```
Remove-AzServiceFabricApplicationType [-ResourceGroupName] <String> [-ClusterName] <String> [-Name <String>]
 [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ef379-108">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="ef379-108">ByResourceId</span></span>
```
Remove-AzServiceFabricApplicationType -ResourceId <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ef379-109">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="ef379-109">ByInputObject</span></span>
```
Remove-AzServiceFabricApplicationType -InputObject <PSApplicationType> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ef379-110">설명</span><span class="sxs-lookup"><span data-stu-id="ef379-110">DESCRIPTION</span></span>
<span data-ttu-id="ef379-111">이 cmdlet은 클러스터 형식을 제거하고 이 리소스에서 모든 형식 버전을 제거하지만 이 명령을 실행하기 전에 해당 리소스의 모든 애플리케이션을 제거해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="ef379-111">This cmdlet removes an application type form the cluster and will remove all type version under this resource, but all applications under it should be removed before running this command.</span></span>

## <span data-ttu-id="ef379-112">예제</span><span class="sxs-lookup"><span data-stu-id="ef379-112">EXAMPLES</span></span>

### <span data-ttu-id="ef379-113">예제 1</span><span class="sxs-lookup"><span data-stu-id="ef379-113">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appTypeName = "testAppType"
PS C:\> Remove-AzServiceFabricApplicationType -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appTypeName -Verbose
```

<span data-ttu-id="ef379-114">이 예제에서는 애플리케이션 유형 "testAppType"과 해당 응용 프로그램 아래에 있는 모든 버전을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="ef379-114">This example will remove the application type "testAppType" and all the version under it.</span></span> <span data-ttu-id="ef379-115">이 형식을 사용하여 만든 애플리케이션이 있는 경우 명령은 예외를 throw합니다.</span><span class="sxs-lookup"><span data-stu-id="ef379-115">If there are any applications created with this type, the command will throw an exception.</span></span>

## <span data-ttu-id="ef379-116">매개 변수</span><span class="sxs-lookup"><span data-stu-id="ef379-116">PARAMETERS</span></span>

### <span data-ttu-id="ef379-117">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="ef379-117">-ClusterName</span></span>
<span data-ttu-id="ef379-118">클러스터의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ef379-118">Specify the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroup
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ef379-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef379-119">-DefaultProfile</span></span>
<span data-ttu-id="ef379-120">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ef379-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ef379-121">-Force</span><span class="sxs-lookup"><span data-stu-id="ef379-121">-Force</span></span>
<span data-ttu-id="ef379-122">프롬프트 없이 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="ef379-122">Remove without prompt.</span></span>

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

### <span data-ttu-id="ef379-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ef379-123">-InputObject</span></span>
<span data-ttu-id="ef379-124">애플리케이션 형식 리소스입니다.</span><span class="sxs-lookup"><span data-stu-id="ef379-124">The application type resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceFabric.Models.PSApplicationType
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ef379-125">-Name</span><span class="sxs-lookup"><span data-stu-id="ef379-125">-Name</span></span>
<span data-ttu-id="ef379-126">애플리케이션 형식의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ef379-126">Specify the name of the application type.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroup
Aliases: ApplicationTypeName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef379-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ef379-127">-PassThru</span></span>
<span data-ttu-id="ef379-128">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="ef379-128">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="ef379-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ef379-129">-ResourceGroupName</span></span>
<span data-ttu-id="ef379-130">리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ef379-130">Specify the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroup
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ef379-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ef379-131">-ResourceId</span></span>
<span data-ttu-id="ef379-132">애플리케이션 형식의 Arm ResourceId입니다.</span><span class="sxs-lookup"><span data-stu-id="ef379-132">Arm ResourceId of the application type.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ef379-133">-확인</span><span class="sxs-lookup"><span data-stu-id="ef379-133">-Confirm</span></span>
<span data-ttu-id="ef379-134">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="ef379-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ef379-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ef379-135">-WhatIf</span></span>
<span data-ttu-id="ef379-136">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="ef379-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ef379-137">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ef379-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ef379-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef379-138">CommonParameters</span></span>
<span data-ttu-id="ef379-139">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="ef379-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef379-140">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ef379-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef379-141">입력</span><span class="sxs-lookup"><span data-stu-id="ef379-141">INPUTS</span></span>

### <span data-ttu-id="ef379-142">System.String</span><span class="sxs-lookup"><span data-stu-id="ef379-142">System.String</span></span>

### <span data-ttu-id="ef379-143">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplicationType</span><span class="sxs-lookup"><span data-stu-id="ef379-143">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplicationType</span></span>

## <span data-ttu-id="ef379-144">출력</span><span class="sxs-lookup"><span data-stu-id="ef379-144">OUTPUTS</span></span>

### <span data-ttu-id="ef379-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="ef379-145">System.Boolean</span></span>

## <span data-ttu-id="ef379-146">참고 사항</span><span class="sxs-lookup"><span data-stu-id="ef379-146">NOTES</span></span>

## <span data-ttu-id="ef379-147">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ef379-147">RELATED LINKS</span></span>
