---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/new-azservicefabricapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/New-AzServiceFabricApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/New-AzServiceFabricApplication.md
ms.openlocfilehash: 5295caae4ffa0138a1c81fd08a5614f6e636eb41
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98494779"
---
# <span data-ttu-id="1c9b4-101">New-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="1c9b4-101">New-AzServiceFabricApplication</span></span>

## <span data-ttu-id="1c9b4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1c9b4-102">SYNOPSIS</span></span>
<span data-ttu-id="1c9b4-103">지정된 리소스 그룹 및 클러스터 아래에 새 Service Fabric 애플리케이션을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1c9b4-103">Create new service fabric application under the specified resource group and cluster.</span></span>

## <span data-ttu-id="1c9b4-104">구문</span><span class="sxs-lookup"><span data-stu-id="1c9b4-104">SYNTAX</span></span>

### <span data-ttu-id="1c9b4-105">SkipAppTypeVersion(기본값)</span><span class="sxs-lookup"><span data-stu-id="1c9b4-105">SkipAppTypeVersion (Default)</span></span>
```
New-AzServiceFabricApplication [-ResourceGroupName] <String> [-ClusterName] <String>
 [-ApplicationTypeName] <String> [-ApplicationTypeVersion] <String> -Name <String>
 [-ApplicationParameter <Hashtable>] [-MinimumNodeCount <Int64>] [-MaximumNodeCount <Int64>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1c9b4-106">CreateAppTypeVersion</span><span class="sxs-lookup"><span data-stu-id="1c9b4-106">CreateAppTypeVersion</span></span>
```
New-AzServiceFabricApplication [-ResourceGroupName] <String> [-ClusterName] <String>
 [-ApplicationTypeName] <String> [-ApplicationTypeVersion] <String> -Name <String>
 [-ApplicationParameter <Hashtable>] -PackageUrl <String> [-MinimumNodeCount <Int64>]
 [-MaximumNodeCount <Int64>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1c9b4-107">설명</span><span class="sxs-lookup"><span data-stu-id="1c9b4-107">DESCRIPTION</span></span>
<span data-ttu-id="1c9b4-108">이 cmdlet은 지정된 리소스 그룹 및 클러스터 아래에 새 Service Fabric 애플리케이션을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="1c9b4-108">This cmdlet creates a new service fabric application under the specified resource group and cluster.</span></span> <span data-ttu-id="1c9b4-109">-PackageUrl 매개 변수를 사용하여 형식 버전을 만들 수 있습니다. 형식 버전이 이미 종료되지만 '실패' 상태인 경우 cmdlet은 사용자가 형식 버전을 다시 만들지 묻습니다.</span><span class="sxs-lookup"><span data-stu-id="1c9b4-109">The parameter -PackageUrl can be used to create the type version, If the type version already exits but its in 'Failed' state the cmdlet will ask if the user wants to recreate the type version.</span></span> <span data-ttu-id="1c9b4-110">'실패' 상태로 계속된 경우 명령은 프로세스를 중지하고 예외를 throw합니다.</span><span class="sxs-lookup"><span data-stu-id="1c9b4-110">If it continues in 'Failed' state, the command will stop the process and throw an exception.</span></span>

## <span data-ttu-id="1c9b4-111">예제</span><span class="sxs-lookup"><span data-stu-id="1c9b4-111">EXAMPLES</span></span>

### <span data-ttu-id="1c9b4-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="1c9b4-112">Example 1</span></span>
```powershell
PS C:\> New-AzServiceFabricApplication -ResourceGroupName "testRG" -ClusterName "testCluster" -ApplicationTypeName "TestAppType" -ApplicationTypeVersion "v1" -Name "testApp" -ApplicationParameter @{key0="value0";key1=$null;key2="value2"}
```

<span data-ttu-id="1c9b4-113">이 예제에서는 리소스 그룹 "testRG" 및 클러스터 "testCluster"에 "testApp" 애플리케이션을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="1c9b4-113">This example creates the application "testApp" under resource group "testRG" and cluster "testCluster".</span></span> <span data-ttu-id="1c9b4-114">애플리케이션 유형 "TestAppType" 버전 "v1"이 클러스터에 이미 존재해야 합니다. 애플리케이션 매개 변수는 애플리케이션 매니페스트에 정의해야 합니다. 그렇지 않으면 cmdlet이 실패합니다.</span><span class="sxs-lookup"><span data-stu-id="1c9b4-114">The application type "TestAppType" version "v1" should already exist in the cluster, and the application parameters should be defined in the application manifest otherwise the cmdlet will fail.</span></span>

### <span data-ttu-id="1c9b4-115">예제 2: 애플리케이션을 만들기 전에 -PackageUrl을 지정하여 애플리케이션 유형 버전을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1c9b4-115">Example 2: Specify -PackageUrl to create the application type version before creating the application.</span></span>
```powershell
PS C:\> New-AzServiceFabricApplication -ResourceGroupName "testRG" -ClusterName "testCluster" -ApplicationTypeName "TestAppType" -ApplicationTypeVersion "v1" -Name "testApp" -PackageUrl "https://sftestapp.blob.core.windows.net/sftestapp/testApp_1.0.sfpkg" -ApplicationParameter @{key0="value0";key1=$null;key2="value2"}
```

<span data-ttu-id="1c9b4-116">이 예제에서는 제공된 패키지 URL을 사용하여 애플리케이션 유형 "TestAppType" 버전 "v1"을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="1c9b4-116">This example creates the application type "TestAppType"  version "v1" using the package url provided.</span></span> <span data-ttu-id="1c9b4-117">그런 다음 애플리케이션을 만드는 일반적인 프로세스를 계속합니다.</span><span class="sxs-lookup"><span data-stu-id="1c9b4-117">After this, it will continue the normal process to create the application.</span></span> <span data-ttu-id="1c9b4-118">애플리케이션 형식 버전이 이미 종료되어 프로비전 상태가 '실패'인 경우 사용자가 형식 버전을 다시 사용할지 여부를 결정하라는 메시지가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1c9b4-118">If the application type version already exits and the provisioning state its in 'Failed' it will prompt to decide if the user wants to recreate the type version.</span></span>

## <span data-ttu-id="1c9b4-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1c9b4-119">PARAMETERS</span></span>

### <span data-ttu-id="1c9b4-120">-ApplicationParameter</span><span class="sxs-lookup"><span data-stu-id="1c9b4-120">-ApplicationParameter</span></span>
<span data-ttu-id="1c9b4-121">애플리케이션 매개 변수를 키/값 쌍으로 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="1c9b4-121">Specify the application parameters as key/value pairs.</span></span>
<span data-ttu-id="1c9b4-122">이러한 매개 변수는 애플리케이션 매니페스트에 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="1c9b4-122">These parameters must exist in the application manifest.</span></span>

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

### <span data-ttu-id="1c9b4-123">-ApplicationTypeName</span><span class="sxs-lookup"><span data-stu-id="1c9b4-123">-ApplicationTypeName</span></span>
<span data-ttu-id="1c9b4-124">애플리케이션 형식의 이름 지정</span><span class="sxs-lookup"><span data-stu-id="1c9b4-124">Specify the name of the application type</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1c9b4-125">-ApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="1c9b4-125">-ApplicationTypeVersion</span></span>
<span data-ttu-id="1c9b4-126">애플리케이션 유형 버전 지정</span><span class="sxs-lookup"><span data-stu-id="1c9b4-126">Specify the application type version</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1c9b4-127">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="1c9b4-127">-ClusterName</span></span>
<span data-ttu-id="1c9b4-128">클러스터의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="1c9b4-128">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="1c9b4-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1c9b4-129">-DefaultProfile</span></span>
<span data-ttu-id="1c9b4-130">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="1c9b4-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1c9b4-131">-Force</span><span class="sxs-lookup"><span data-stu-id="1c9b4-131">-Force</span></span>
<span data-ttu-id="1c9b4-132">프롬프트 없이 계속</span><span class="sxs-lookup"><span data-stu-id="1c9b4-132">Continue without prompts</span></span>

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

### <span data-ttu-id="1c9b4-133">-MaximumNodeCount</span><span class="sxs-lookup"><span data-stu-id="1c9b4-133">-MaximumNodeCount</span></span>
<span data-ttu-id="1c9b4-134">애플리케이션을 두는 노드의 최대 수를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="1c9b4-134">Specifies the maximum number of nodes on which to place an application</span></span>

```yaml
Type: System.Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1c9b4-135">-MinimumNodeCount</span><span class="sxs-lookup"><span data-stu-id="1c9b4-135">-MinimumNodeCount</span></span>
<span data-ttu-id="1c9b4-136">Service Fabric이 이 애플리케이션에 대한 용량을 예약하는 노드의 최소 수를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="1c9b4-136">Specifies the minimum number of nodes where Service Fabric will reserve capacity for this application</span></span>

```yaml
Type: System.Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1c9b4-137">-Name</span><span class="sxs-lookup"><span data-stu-id="1c9b4-137">-Name</span></span>
<span data-ttu-id="1c9b4-138">애플리케이션의 이름 지정</span><span class="sxs-lookup"><span data-stu-id="1c9b4-138">Specify the name of the application</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ApplicationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1c9b4-139">-PackageUrl</span><span class="sxs-lookup"><span data-stu-id="1c9b4-139">-PackageUrl</span></span>
<span data-ttu-id="1c9b4-140">애플리케이션 패키지 sfpkg 파일의 URL 지정</span><span class="sxs-lookup"><span data-stu-id="1c9b4-140">Specify the url of the application package sfpkg file</span></span>

```yaml
Type: System.String
Parameter Sets: CreateAppTypeVersion
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1c9b4-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1c9b4-141">-ResourceGroupName</span></span>
<span data-ttu-id="1c9b4-142">리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="1c9b4-142">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="1c9b4-143">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1c9b4-143">-Confirm</span></span>
<span data-ttu-id="1c9b4-144">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="1c9b4-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1c9b4-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1c9b4-145">-WhatIf</span></span>
<span data-ttu-id="1c9b4-146">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="1c9b4-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1c9b4-147">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1c9b4-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1c9b4-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c9b4-148">CommonParameters</span></span>
<span data-ttu-id="1c9b4-149">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="1c9b4-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c9b4-150">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="1c9b4-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c9b4-151">입력</span><span class="sxs-lookup"><span data-stu-id="1c9b4-151">INPUTS</span></span>

### <span data-ttu-id="1c9b4-152">System.String</span><span class="sxs-lookup"><span data-stu-id="1c9b4-152">System.String</span></span>

### <span data-ttu-id="1c9b4-153">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="1c9b4-153">System.Collections.Hashtable</span></span>

## <span data-ttu-id="1c9b4-154">출력</span><span class="sxs-lookup"><span data-stu-id="1c9b4-154">OUTPUTS</span></span>

### <span data-ttu-id="1c9b4-155">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplication</span><span class="sxs-lookup"><span data-stu-id="1c9b4-155">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplication</span></span>

## <span data-ttu-id="1c9b4-156">참고 사항</span><span class="sxs-lookup"><span data-stu-id="1c9b4-156">NOTES</span></span>

## <span data-ttu-id="1c9b4-157">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1c9b4-157">RELATED LINKS</span></span>
