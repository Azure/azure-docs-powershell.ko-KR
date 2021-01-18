---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/new-azservicefabricapplicationtypeversion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/New-AzServiceFabricApplicationTypeVersion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/New-AzServiceFabricApplicationTypeVersion.md
ms.openlocfilehash: 60065541ecdd8439b67f4370bc1ef8bdc24119bc
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98494776"
---
# <span data-ttu-id="63234-101">New-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="63234-101">New-AzServiceFabricApplicationTypeVersion</span></span>

## <span data-ttu-id="63234-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="63234-102">SYNOPSIS</span></span>
<span data-ttu-id="63234-103">지정된 리소스 그룹 및 클러스터에서 새 애플리케이션 유형 버전을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="63234-103">Create new application type version under the specified resource group and cluster.</span></span>

## <span data-ttu-id="63234-104">구문</span><span class="sxs-lookup"><span data-stu-id="63234-104">SYNTAX</span></span>

```
New-AzServiceFabricApplicationTypeVersion [-ResourceGroupName] <String> [-ClusterName] <String>
 [-Name] <String> [-Version] <String> -PackageUrl <String> [-DefaultParameter <Hashtable>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="63234-105">설명</span><span class="sxs-lookup"><span data-stu-id="63234-105">DESCRIPTION</span></span>
<span data-ttu-id="63234-106">이 cmdlet은 -PackageUrl에 지정된 패키지를 사용하여 새 애플리케이션 유형 버전을 만듭니다. 배포 중에 사용할 Azure Resource Manager의 REST 엔드포인트를 통해 액세스할 수 있으며 확장 .sfpkg로 패키지 및 압축된 애플리케이션을 포함해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="63234-106">This cmdlet creates a new application type version using the package specified in -PackageUrl, this should be accessible through a REST endpoint for Azure Resource Manager to consume during deployment and contained The application packaged and zipped with the extension .sfpkg.</span></span> <span data-ttu-id="63234-107">이 명령은 애플리케이션 유형이 아직 없는 경우 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="63234-107">This command will create the application type if it doesn't exist already.</span></span>

## <span data-ttu-id="63234-108">예제</span><span class="sxs-lookup"><span data-stu-id="63234-108">EXAMPLES</span></span>

### <span data-ttu-id="63234-109">예제 1</span><span class="sxs-lookup"><span data-stu-id="63234-109">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appTypeName = "testAppType"
PS C:\> $version = "v1"
PS C:\> $packageUrl = "https://sftestapp.blob.core.windows.net/sftestapp/testApp_1.0.sfpkg"
PS C:\> New-AzServiceFabricApplicationTypeVersion -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appTypeName -Version $version -PackageUrl $packageUrl -Verbose
```

<span data-ttu-id="63234-110">이 예제에서는 "testAppType" 형식 아래에 애플리케이션 유형 버전 "v1"을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="63234-110">This example will create an application type version "v1" under type "testAppType".</span></span> <span data-ttu-id="63234-111">패키지에 포함된 애플리케이션 매니페스트의 버전은 -Version에 지정된 버전과 동일한 버전을 포함해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="63234-111">The version in the application manifest contained in the package should have the same version as the one specified in -Version.</span></span>

## <span data-ttu-id="63234-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="63234-112">PARAMETERS</span></span>

### <span data-ttu-id="63234-113">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="63234-113">-ClusterName</span></span>
<span data-ttu-id="63234-114">클러스터의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="63234-114">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="63234-115">-DefaultParameter</span><span class="sxs-lookup"><span data-stu-id="63234-115">-DefaultParameter</span></span>
<span data-ttu-id="63234-116">애플리케이션 매개 변수의 기본값을 키/값 쌍으로 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="63234-116">Specify the default values of the application parameters as key/value pairs.</span></span>
<span data-ttu-id="63234-117">이러한 매개 변수는 애플리케이션 매니페스트에 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="63234-117">These parameters must exist in the application manifest.</span></span>

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

### <span data-ttu-id="63234-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="63234-118">-DefaultProfile</span></span>
<span data-ttu-id="63234-119">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="63234-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="63234-120">-Force</span><span class="sxs-lookup"><span data-stu-id="63234-120">-Force</span></span>
<span data-ttu-id="63234-121">프롬프트 없이 계속</span><span class="sxs-lookup"><span data-stu-id="63234-121">Continue without prompts</span></span>

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

### <span data-ttu-id="63234-122">-Name</span><span class="sxs-lookup"><span data-stu-id="63234-122">-Name</span></span>
<span data-ttu-id="63234-123">애플리케이션 형식의 이름 지정</span><span class="sxs-lookup"><span data-stu-id="63234-123">Specify the name of the application type</span></span>

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

### <span data-ttu-id="63234-124">-PackageUrl</span><span class="sxs-lookup"><span data-stu-id="63234-124">-PackageUrl</span></span>
<span data-ttu-id="63234-125">애플리케이션 패키지 sfpkg 파일의 URL 지정</span><span class="sxs-lookup"><span data-stu-id="63234-125">Specify the url of the application package sfpkg file</span></span>

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

### <span data-ttu-id="63234-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="63234-126">-ResourceGroupName</span></span>
<span data-ttu-id="63234-127">리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="63234-127">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="63234-128">-Version</span><span class="sxs-lookup"><span data-stu-id="63234-128">-Version</span></span>
<span data-ttu-id="63234-129">애플리케이션 유형 버전 지정</span><span class="sxs-lookup"><span data-stu-id="63234-129">Specify the application type version</span></span>

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

### <span data-ttu-id="63234-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="63234-130">-Confirm</span></span>
<span data-ttu-id="63234-131">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="63234-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="63234-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="63234-132">-WhatIf</span></span>
<span data-ttu-id="63234-133">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="63234-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="63234-134">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="63234-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="63234-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="63234-135">CommonParameters</span></span>
<span data-ttu-id="63234-136">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="63234-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="63234-137">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="63234-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="63234-138">입력</span><span class="sxs-lookup"><span data-stu-id="63234-138">INPUTS</span></span>

### <span data-ttu-id="63234-139">System.String</span><span class="sxs-lookup"><span data-stu-id="63234-139">System.String</span></span>

### <span data-ttu-id="63234-140">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="63234-140">System.Collections.Hashtable</span></span>

## <span data-ttu-id="63234-141">출력</span><span class="sxs-lookup"><span data-stu-id="63234-141">OUTPUTS</span></span>

### <span data-ttu-id="63234-142">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="63234-142">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplicationTypeVersion</span></span>

## <span data-ttu-id="63234-143">참고 사항</span><span class="sxs-lookup"><span data-stu-id="63234-143">NOTES</span></span>

## <span data-ttu-id="63234-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="63234-144">RELATED LINKS</span></span>
