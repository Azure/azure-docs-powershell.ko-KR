---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/remove-azservicefabricapplicationtypeversion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricApplicationTypeVersion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricApplicationTypeVersion.md
ms.openlocfilehash: 5ab0499ce3fe98a541031b78e2b432de5a2a39dc
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100189097"
---
# <span data-ttu-id="aa786-101">Remove-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="aa786-101">Remove-AzServiceFabricApplicationTypeVersion</span></span>

## <span data-ttu-id="aa786-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aa786-102">SYNOPSIS</span></span>
<span data-ttu-id="aa786-103">클러스터에서 Service Fabric 애플리케이션 유형 버전을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="aa786-103">Remove Service fabric an application type version from the cluster.</span></span> <span data-ttu-id="aa786-104">배포된 ARM 버전만 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="aa786-104">Only supports ARM deployed application type versions.</span></span>

## <span data-ttu-id="aa786-105">구문</span><span class="sxs-lookup"><span data-stu-id="aa786-105">SYNTAX</span></span>

### <span data-ttu-id="aa786-106">ByResourceGroup(기본값)</span><span class="sxs-lookup"><span data-stu-id="aa786-106">ByResourceGroup (Default)</span></span>
```
Remove-AzServiceFabricApplicationTypeVersion [-ResourceGroupName] <String> [-ClusterName] <String>
 -Name <String> -Version <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aa786-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="aa786-107">ByResourceId</span></span>
```
Remove-AzServiceFabricApplicationTypeVersion -ResourceId <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aa786-108">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="aa786-108">ByInputObject</span></span>
```
Remove-AzServiceFabricApplicationTypeVersion -InputObject <PSApplicationTypeVersion> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="aa786-109">설명</span><span class="sxs-lookup"><span data-stu-id="aa786-109">DESCRIPTION</span></span>
<span data-ttu-id="aa786-110">이 cmdlet은 클러스터에서 Service Fabric 애플리케이션 유형 버전을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="aa786-110">This cmdlet will remove Service fabric an application type version from the cluster.</span></span> <span data-ttu-id="aa786-111">이 명령을 실행하기 전에 이 리소스의 모든 애플리케이션을 제거해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="aa786-111">All applications under this resource must be removed before running this command.</span></span>

## <span data-ttu-id="aa786-112">예제</span><span class="sxs-lookup"><span data-stu-id="aa786-112">EXAMPLES</span></span>

### <span data-ttu-id="aa786-113">예제 1</span><span class="sxs-lookup"><span data-stu-id="aa786-113">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appTypeName = "testAppType"
PS C:\> $version = "v1"
PS C:\> Remove-AzServiceFabricApplicationTypeVersion -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appTypeName -Version $version -Force -PassThru -Verbose
```

<span data-ttu-id="aa786-114">이 예제에서는 "testAppType" 형식에서 버전 "v1"을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="aa786-114">This example will remove the version "v1" under the type "testAppType".</span></span> <span data-ttu-id="aa786-115">이 리소스 아래에는 명령이 예외를 throw하는 애플리케이션이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="aa786-115">It there are any applications under this resource the command will throw an exception.</span></span>

## <span data-ttu-id="aa786-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="aa786-116">PARAMETERS</span></span>

### <span data-ttu-id="aa786-117">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="aa786-117">-ClusterName</span></span>
<span data-ttu-id="aa786-118">클러스터의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="aa786-118">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="aa786-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aa786-119">-DefaultProfile</span></span>
<span data-ttu-id="aa786-120">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="aa786-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="aa786-121">-Force</span><span class="sxs-lookup"><span data-stu-id="aa786-121">-Force</span></span>
<span data-ttu-id="aa786-122">프롬프트 없이 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="aa786-122">Remove without prompt.</span></span>

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

### <span data-ttu-id="aa786-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="aa786-123">-InputObject</span></span>
<span data-ttu-id="aa786-124">애플리케이션 유형 버전 리소스입니다.</span><span class="sxs-lookup"><span data-stu-id="aa786-124">The application type version resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceFabric.Models.PSApplicationTypeVersion
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="aa786-125">-Name</span><span class="sxs-lookup"><span data-stu-id="aa786-125">-Name</span></span>
<span data-ttu-id="aa786-126">애플리케이션 형식의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="aa786-126">Specify the name of the application type.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroup
Aliases: ApplicationTypeName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aa786-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="aa786-127">-PassThru</span></span>
<span data-ttu-id="aa786-128">{{PassThru 설명 채우기}}</span><span class="sxs-lookup"><span data-stu-id="aa786-128">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="aa786-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aa786-129">-ResourceGroupName</span></span>
<span data-ttu-id="aa786-130">리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="aa786-130">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="aa786-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="aa786-131">-ResourceId</span></span>
<span data-ttu-id="aa786-132">애플리케이션 형식 버전의 Arm ResourceId입니다.</span><span class="sxs-lookup"><span data-stu-id="aa786-132">Arm ResourceId of the application type version.</span></span>

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

### <span data-ttu-id="aa786-133">-Version</span><span class="sxs-lookup"><span data-stu-id="aa786-133">-Version</span></span>
<span data-ttu-id="aa786-134">애플리케이션 유형 버전을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="aa786-134">Specify the application type version.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroup
Aliases: ApplicationTypeVersion

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aa786-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="aa786-135">-Confirm</span></span>
<span data-ttu-id="aa786-136">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="aa786-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aa786-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aa786-137">-WhatIf</span></span>
<span data-ttu-id="aa786-138">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="aa786-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aa786-139">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="aa786-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aa786-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aa786-140">CommonParameters</span></span>
<span data-ttu-id="aa786-141">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="aa786-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aa786-142">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="aa786-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aa786-143">입력</span><span class="sxs-lookup"><span data-stu-id="aa786-143">INPUTS</span></span>

### <span data-ttu-id="aa786-144">System.String</span><span class="sxs-lookup"><span data-stu-id="aa786-144">System.String</span></span>

### <span data-ttu-id="aa786-145">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="aa786-145">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplicationTypeVersion</span></span>

## <span data-ttu-id="aa786-146">출력</span><span class="sxs-lookup"><span data-stu-id="aa786-146">OUTPUTS</span></span>

### <span data-ttu-id="aa786-147">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="aa786-147">System.Boolean</span></span>

## <span data-ttu-id="aa786-148">참고 사항</span><span class="sxs-lookup"><span data-stu-id="aa786-148">NOTES</span></span>

## <span data-ttu-id="aa786-149">관련 링크</span><span class="sxs-lookup"><span data-stu-id="aa786-149">RELATED LINKS</span></span>
