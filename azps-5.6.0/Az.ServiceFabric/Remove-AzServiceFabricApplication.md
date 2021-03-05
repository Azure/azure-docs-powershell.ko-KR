---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/powershell/module/az.servicefabric/remove-azservicefabricapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricApplication.md
ms.openlocfilehash: 5004b6b9528eb91a1883805405dba6147d5161a1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102005584"
---
# <span data-ttu-id="ec6cc-101">Remove-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="ec6cc-101">Remove-AzServiceFabricApplication</span></span>

## <span data-ttu-id="ec6cc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ec6cc-102">SYNOPSIS</span></span>
<span data-ttu-id="ec6cc-103">클러스터에서 애플리케이션을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="ec6cc-103">Remove an application from the cluster.</span></span> <span data-ttu-id="ec6cc-104">이렇게 하면 애플리케이션에서 모든 서비스가 제거됩니다.</span><span class="sxs-lookup"><span data-stu-id="ec6cc-104">This will remove all the services under the application.</span></span> <span data-ttu-id="ec6cc-105">배포된 애플리케이션만 ARM 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="ec6cc-105">Only supports ARM deployed applications.</span></span>

## <span data-ttu-id="ec6cc-106">구문</span><span class="sxs-lookup"><span data-stu-id="ec6cc-106">SYNTAX</span></span>

### <span data-ttu-id="ec6cc-107">ByResourceGroup(기본값)</span><span class="sxs-lookup"><span data-stu-id="ec6cc-107">ByResourceGroup (Default)</span></span>
```
Remove-AzServiceFabricApplication [-ResourceGroupName] <String> [-ClusterName] <String> [-Name] <String>
 [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ec6cc-108">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="ec6cc-108">ByResourceId</span></span>
```
Remove-AzServiceFabricApplication -ResourceId <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ec6cc-109">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="ec6cc-109">ByInputObject</span></span>
```
Remove-AzServiceFabricApplication -InputObject <PSApplication> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ec6cc-110">설명</span><span class="sxs-lookup"><span data-stu-id="ec6cc-110">DESCRIPTION</span></span>
<span data-ttu-id="ec6cc-111">이 cmdlet은 애플리케이션 양식 클러스터를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="ec6cc-111">This cmdlet removes an application form the cluster.</span></span> <span data-ttu-id="ec6cc-112">그러면 애플리케이션 리소스 아래에서 모든 서비스가 제거됩니다.</span><span class="sxs-lookup"><span data-stu-id="ec6cc-112">This will remove all the services, if any, under the application resource.</span></span>

## <span data-ttu-id="ec6cc-113">예제</span><span class="sxs-lookup"><span data-stu-id="ec6cc-113">EXAMPLES</span></span>

### <span data-ttu-id="ec6cc-114">예제 1</span><span class="sxs-lookup"><span data-stu-id="ec6cc-114">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appName = "testApp"
PS C:\> Remove-AzServiceFabricApplication -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appName
```

<span data-ttu-id="ec6cc-115">이 예제에서는 리소스 그룹 "testRG" 및 클러스터 "testCluster"에서 애플리케이션 "testApp"을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="ec6cc-115">This example removes the application "testApp" under the resource group "testRG" and cluster "testCluster".</span></span>

## <span data-ttu-id="ec6cc-116">매개 변수</span><span class="sxs-lookup"><span data-stu-id="ec6cc-116">PARAMETERS</span></span>

### <span data-ttu-id="ec6cc-117">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="ec6cc-117">-ClusterName</span></span>
<span data-ttu-id="ec6cc-118">클러스터의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ec6cc-118">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="ec6cc-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ec6cc-119">-DefaultProfile</span></span>
<span data-ttu-id="ec6cc-120">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ec6cc-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ec6cc-121">-Force</span><span class="sxs-lookup"><span data-stu-id="ec6cc-121">-Force</span></span>
<span data-ttu-id="ec6cc-122">프롬프트 없이 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="ec6cc-122">Remove without prompt.</span></span>

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

### <span data-ttu-id="ec6cc-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ec6cc-123">-InputObject</span></span>
<span data-ttu-id="ec6cc-124">애플리케이션 리소스입니다.</span><span class="sxs-lookup"><span data-stu-id="ec6cc-124">The application resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceFabric.Models.PSApplication
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ec6cc-125">-Name</span><span class="sxs-lookup"><span data-stu-id="ec6cc-125">-Name</span></span>
<span data-ttu-id="ec6cc-126">애플리케이션의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ec6cc-126">Specify the name of the application.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroup
Aliases: ApplicationName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec6cc-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ec6cc-127">-PassThru</span></span>
<span data-ttu-id="ec6cc-128">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="ec6cc-128">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="ec6cc-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ec6cc-129">-ResourceGroupName</span></span>
<span data-ttu-id="ec6cc-130">리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ec6cc-130">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="ec6cc-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ec6cc-131">-ResourceId</span></span>
<span data-ttu-id="ec6cc-132">애플리케이션의 Arm ResourceId입니다.</span><span class="sxs-lookup"><span data-stu-id="ec6cc-132">Arm ResourceId of the application.</span></span>

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

### <span data-ttu-id="ec6cc-133">-확인</span><span class="sxs-lookup"><span data-stu-id="ec6cc-133">-Confirm</span></span>
<span data-ttu-id="ec6cc-134">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="ec6cc-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ec6cc-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ec6cc-135">-WhatIf</span></span>
<span data-ttu-id="ec6cc-136">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="ec6cc-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ec6cc-137">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ec6cc-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ec6cc-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec6cc-138">CommonParameters</span></span>
<span data-ttu-id="ec6cc-139">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="ec6cc-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec6cc-140">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ec6cc-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec6cc-141">입력</span><span class="sxs-lookup"><span data-stu-id="ec6cc-141">INPUTS</span></span>

### <span data-ttu-id="ec6cc-142">System.String</span><span class="sxs-lookup"><span data-stu-id="ec6cc-142">System.String</span></span>

### <span data-ttu-id="ec6cc-143">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplication</span><span class="sxs-lookup"><span data-stu-id="ec6cc-143">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplication</span></span>

## <span data-ttu-id="ec6cc-144">출력</span><span class="sxs-lookup"><span data-stu-id="ec6cc-144">OUTPUTS</span></span>

### <span data-ttu-id="ec6cc-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="ec6cc-145">System.Boolean</span></span>

## <span data-ttu-id="ec6cc-146">참고 사항</span><span class="sxs-lookup"><span data-stu-id="ec6cc-146">NOTES</span></span>

## <span data-ttu-id="ec6cc-147">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ec6cc-147">RELATED LINKS</span></span>
