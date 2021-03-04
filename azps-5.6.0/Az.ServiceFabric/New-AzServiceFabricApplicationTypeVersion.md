---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/powershell/module/az.servicefabric/new-azservicefabricapplicationtypeversion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/New-AzServiceFabricApplicationTypeVersion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/New-AzServiceFabricApplicationTypeVersion.md
ms.openlocfilehash: d13e2e4473c390a27be4741de703818bda769efa
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101959371"
---
# <span data-ttu-id="efb5d-101">New-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="efb5d-101">New-AzServiceFabricApplicationTypeVersion</span></span>

## <span data-ttu-id="efb5d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="efb5d-102">SYNOPSIS</span></span>
<span data-ttu-id="efb5d-103">지정된 리소스 그룹 및 클러스터 아래에서 새 애플리케이션 형식 버전을 만드면 됩니다.</span><span class="sxs-lookup"><span data-stu-id="efb5d-103">Create new application type version under the specified resource group and cluster.</span></span>

## <span data-ttu-id="efb5d-104">구문</span><span class="sxs-lookup"><span data-stu-id="efb5d-104">SYNTAX</span></span>

```
New-AzServiceFabricApplicationTypeVersion [-ResourceGroupName] <String> [-ClusterName] <String>
 [-Name] <String> [-Version] <String> -PackageUrl <String> [-DefaultParameter <Hashtable>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="efb5d-105">설명</span><span class="sxs-lookup"><span data-stu-id="efb5d-105">DESCRIPTION</span></span>
<span data-ttu-id="efb5d-106">이 cmdlet은 -PackageUrl에 지정된 패키지를 사용하여 새 애플리케이션 형식 버전을 만듭니다. 이 버전은 Azure Resource Manager의 REST 엔드포인트를 통해 배포 중에 사용할 수 있으며 확장 .sfpkg로 애플리케이션 패키지 및 압축을 포함해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="efb5d-106">This cmdlet creates a new application type version using the package specified in -PackageUrl, this should be accessible through a REST endpoint for Azure Resource Manager to consume during deployment and contained The application packaged and zipped with the extension .sfpkg.</span></span> <span data-ttu-id="efb5d-107">이 명령은 애플리케이션 형식이 아직 없는 경우 생성됩니다.</span><span class="sxs-lookup"><span data-stu-id="efb5d-107">This command will create the application type if it doesn't exist already.</span></span>

## <span data-ttu-id="efb5d-108">예제</span><span class="sxs-lookup"><span data-stu-id="efb5d-108">EXAMPLES</span></span>

### <span data-ttu-id="efb5d-109">예제 1</span><span class="sxs-lookup"><span data-stu-id="efb5d-109">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appTypeName = "testAppType"
PS C:\> $version = "v1"
PS C:\> $packageUrl = "https://sftestapp.blob.core.windows.net/sftestapp/testApp_1.0.sfpkg"
PS C:\> New-AzServiceFabricApplicationTypeVersion -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appTypeName -Version $version -PackageUrl $packageUrl -Verbose
```

<span data-ttu-id="efb5d-110">이 예제에서는 "testAppType"을 입력하여 애플리케이션 형식 버전 "v1"을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="efb5d-110">This example will create an application type version "v1" under type "testAppType".</span></span> <span data-ttu-id="efb5d-111">패키지에 포함된 애플리케이션 매니페스트의 버전은 -Version에 지정된 버전과 동일해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="efb5d-111">The version in the application manifest contained in the package should have the same version as the one specified in -Version.</span></span>

## <span data-ttu-id="efb5d-112">매개 변수</span><span class="sxs-lookup"><span data-stu-id="efb5d-112">PARAMETERS</span></span>

### <span data-ttu-id="efb5d-113">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="efb5d-113">-ClusterName</span></span>
<span data-ttu-id="efb5d-114">클러스터의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="efb5d-114">Specify the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="efb5d-115">-DefaultParameter</span><span class="sxs-lookup"><span data-stu-id="efb5d-115">-DefaultParameter</span></span>
<span data-ttu-id="efb5d-116">애플리케이션 매개 변수의 기본값을 키/값 쌍으로 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="efb5d-116">Specify the default values of the application parameters as key/value pairs.</span></span>
<span data-ttu-id="efb5d-117">이러한 매개 변수는 애플리케이션 매니페스트에 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="efb5d-117">These parameters must exist in the application manifest.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="efb5d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="efb5d-118">-DefaultProfile</span></span>
<span data-ttu-id="efb5d-119">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="efb5d-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="efb5d-120">-Force</span><span class="sxs-lookup"><span data-stu-id="efb5d-120">-Force</span></span>
<span data-ttu-id="efb5d-121">프롬프트 없이 계속 진행</span><span class="sxs-lookup"><span data-stu-id="efb5d-121">Continue without prompts</span></span>

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

### <span data-ttu-id="efb5d-122">-Name</span><span class="sxs-lookup"><span data-stu-id="efb5d-122">-Name</span></span>
<span data-ttu-id="efb5d-123">애플리케이션 형식의 이름 지정</span><span class="sxs-lookup"><span data-stu-id="efb5d-123">Specify the name of the application type</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ApplicationTypeName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="efb5d-124">-PackageUrl</span><span class="sxs-lookup"><span data-stu-id="efb5d-124">-PackageUrl</span></span>
<span data-ttu-id="efb5d-125">애플리케이션 패키지 sfpkg 파일의 URL 지정</span><span class="sxs-lookup"><span data-stu-id="efb5d-125">Specify the url of the application package sfpkg file</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="efb5d-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="efb5d-126">-ResourceGroupName</span></span>
<span data-ttu-id="efb5d-127">리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="efb5d-127">Specify the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="efb5d-128">-Version</span><span class="sxs-lookup"><span data-stu-id="efb5d-128">-Version</span></span>
<span data-ttu-id="efb5d-129">애플리케이션 유형 버전 지정</span><span class="sxs-lookup"><span data-stu-id="efb5d-129">Specify the application type version</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ApplicationTypeVersion

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="efb5d-130">-확인</span><span class="sxs-lookup"><span data-stu-id="efb5d-130">-Confirm</span></span>
<span data-ttu-id="efb5d-131">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="efb5d-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="efb5d-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="efb5d-132">-WhatIf</span></span>
<span data-ttu-id="efb5d-133">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="efb5d-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="efb5d-134">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="efb5d-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="efb5d-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="efb5d-135">CommonParameters</span></span>
<span data-ttu-id="efb5d-136">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="efb5d-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="efb5d-137">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="efb5d-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="efb5d-138">입력</span><span class="sxs-lookup"><span data-stu-id="efb5d-138">INPUTS</span></span>

### <span data-ttu-id="efb5d-139">System.String</span><span class="sxs-lookup"><span data-stu-id="efb5d-139">System.String</span></span>

### <span data-ttu-id="efb5d-140">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="efb5d-140">System.Collections.Hashtable</span></span>

## <span data-ttu-id="efb5d-141">출력</span><span class="sxs-lookup"><span data-stu-id="efb5d-141">OUTPUTS</span></span>

### <span data-ttu-id="efb5d-142">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="efb5d-142">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplicationTypeVersion</span></span>

## <span data-ttu-id="efb5d-143">참고 사항</span><span class="sxs-lookup"><span data-stu-id="efb5d-143">NOTES</span></span>

## <span data-ttu-id="efb5d-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="efb5d-144">RELATED LINKS</span></span>
