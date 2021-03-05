---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/powershell/module/az.servicefabric/new-azservicefabricapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/New-AzServiceFabricApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/New-AzServiceFabricApplication.md
ms.openlocfilehash: e1e6efbdeaed90fe7591ed2dd5a645955dd5a314
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101982160"
---
# <span data-ttu-id="26316-101">New-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="26316-101">New-AzServiceFabricApplication</span></span>

## <span data-ttu-id="26316-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="26316-102">SYNOPSIS</span></span>
<span data-ttu-id="26316-103">지정된 리소스 그룹 및 클러스터에서 새 서비스 패브릭 애플리케이션을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="26316-103">Create new service fabric application under the specified resource group and cluster.</span></span>

## <span data-ttu-id="26316-104">구문</span><span class="sxs-lookup"><span data-stu-id="26316-104">SYNTAX</span></span>

### <span data-ttu-id="26316-105">SkipAppTypeVersion(기본값)</span><span class="sxs-lookup"><span data-stu-id="26316-105">SkipAppTypeVersion (Default)</span></span>
```
New-AzServiceFabricApplication [-ResourceGroupName] <String> [-ClusterName] <String>
 [-ApplicationTypeName] <String> [-ApplicationTypeVersion] <String> -Name <String>
 [-ApplicationParameter <Hashtable>] [-MinimumNodeCount <Int64>] [-MaximumNodeCount <Int64>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="26316-106">CreateAppTypeVersion</span><span class="sxs-lookup"><span data-stu-id="26316-106">CreateAppTypeVersion</span></span>
```
New-AzServiceFabricApplication [-ResourceGroupName] <String> [-ClusterName] <String>
 [-ApplicationTypeName] <String> [-ApplicationTypeVersion] <String> -Name <String>
 [-ApplicationParameter <Hashtable>] -PackageUrl <String> [-MinimumNodeCount <Int64>]
 [-MaximumNodeCount <Int64>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="26316-107">설명</span><span class="sxs-lookup"><span data-stu-id="26316-107">DESCRIPTION</span></span>
<span data-ttu-id="26316-108">이 cmdlet은 지정된 리소스 그룹 및 클러스터 아래에 새 서비스 패브릭 애플리케이션을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="26316-108">This cmdlet creates a new service fabric application under the specified resource group and cluster.</span></span> <span data-ttu-id="26316-109">매개 변수 -PackageUrl을 사용하여 형식 버전을 만들 수 있습니다. 형식 버전이 이미 종료되지만 '실패' 상태인 경우 cmdlet에서 사용자가 형식 버전을 다시 만들지 묻는 질문을 합니다.</span><span class="sxs-lookup"><span data-stu-id="26316-109">The parameter -PackageUrl can be used to create the type version, If the type version already exits but its in 'Failed' state the cmdlet will ask if the user wants to recreate the type version.</span></span> <span data-ttu-id="26316-110">'실패' 상태로 계속된 경우 명령은 프로세스를 중지하고 예외를 throw합니다.</span><span class="sxs-lookup"><span data-stu-id="26316-110">If it continues in 'Failed' state, the command will stop the process and throw an exception.</span></span>

## <span data-ttu-id="26316-111">예제</span><span class="sxs-lookup"><span data-stu-id="26316-111">EXAMPLES</span></span>

### <span data-ttu-id="26316-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="26316-112">Example 1</span></span>
```powershell
PS C:\> New-AzServiceFabricApplication -ResourceGroupName "testRG" -ClusterName "testCluster" -ApplicationTypeName "TestAppType" -ApplicationTypeVersion "v1" -Name "testApp" -ApplicationParameter @{key0="value0";key1=$null;key2="value2"}
```

<span data-ttu-id="26316-113">이 예제에서는 리소스 그룹 "testRG" 및 클러스터 "testCluster"에서 애플리케이션 "testApp"을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="26316-113">This example creates the application "testApp" under resource group "testRG" and cluster "testCluster".</span></span> <span data-ttu-id="26316-114">애플리케이션 유형 "TestAppType" 버전 "v1"은 클러스터에 이미 존재해야 합니다. 애플리케이션 매개 변수는 애플리케이션 매니페스트에 정의해야 합니다. 그렇지 않으면 cmdlet이 실패합니다.</span><span class="sxs-lookup"><span data-stu-id="26316-114">The application type "TestAppType" version "v1" should already exist in the cluster, and the application parameters should be defined in the application manifest otherwise the cmdlet will fail.</span></span>

### <span data-ttu-id="26316-115">예제 2: 애플리케이션을 만들기 전에 -PackageUrl을 지정하여 애플리케이션 형식 버전을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="26316-115">Example 2: Specify -PackageUrl to create the application type version before creating the application.</span></span>
```powershell
PS C:\> New-AzServiceFabricApplication -ResourceGroupName "testRG" -ClusterName "testCluster" -ApplicationTypeName "TestAppType" -ApplicationTypeVersion "v1" -Name "testApp" -PackageUrl "https://sftestapp.blob.core.windows.net/sftestapp/testApp_1.0.sfpkg" -ApplicationParameter @{key0="value0";key1=$null;key2="value2"}
```

<span data-ttu-id="26316-116">이 예제에서는 제공된 패키지 URL을 사용하여 애플리케이션 형식 "TestAppType" 버전 "v1"을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="26316-116">This example creates the application type "TestAppType"  version "v1" using the package url provided.</span></span> <span data-ttu-id="26316-117">이 후 애플리케이션을 만드는 일반적인 프로세스를 계속합니다.</span><span class="sxs-lookup"><span data-stu-id="26316-117">After this, it will continue the normal process to create the application.</span></span> <span data-ttu-id="26316-118">애플리케이션 형식 버전이 이미 종료되어 프로비전 상태가 '실패'인 경우 사용자가 형식 버전을 다시 사용할지 여부를 결정하라는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="26316-118">If the application type version already exits and the provisioning state its in 'Failed' it will prompt to decide if the user wants to recreate the type version.</span></span>

## <span data-ttu-id="26316-119">매개 변수</span><span class="sxs-lookup"><span data-stu-id="26316-119">PARAMETERS</span></span>

### <span data-ttu-id="26316-120">-ApplicationParameter</span><span class="sxs-lookup"><span data-stu-id="26316-120">-ApplicationParameter</span></span>
<span data-ttu-id="26316-121">애플리케이션 매개 변수를 키/값 쌍으로 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="26316-121">Specify the application parameters as key/value pairs.</span></span>
<span data-ttu-id="26316-122">이러한 매개 변수는 애플리케이션 매니페스트에 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="26316-122">These parameters must exist in the application manifest.</span></span>

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

### <span data-ttu-id="26316-123">-ApplicationTypeName</span><span class="sxs-lookup"><span data-stu-id="26316-123">-ApplicationTypeName</span></span>
<span data-ttu-id="26316-124">애플리케이션 형식의 이름 지정</span><span class="sxs-lookup"><span data-stu-id="26316-124">Specify the name of the application type</span></span>

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

### <span data-ttu-id="26316-125">-ApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="26316-125">-ApplicationTypeVersion</span></span>
<span data-ttu-id="26316-126">애플리케이션 유형 버전 지정</span><span class="sxs-lookup"><span data-stu-id="26316-126">Specify the application type version</span></span>

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

### <span data-ttu-id="26316-127">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="26316-127">-ClusterName</span></span>
<span data-ttu-id="26316-128">클러스터의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="26316-128">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="26316-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26316-129">-DefaultProfile</span></span>
<span data-ttu-id="26316-130">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="26316-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="26316-131">-Force</span><span class="sxs-lookup"><span data-stu-id="26316-131">-Force</span></span>
<span data-ttu-id="26316-132">프롬프트 없이 계속 진행</span><span class="sxs-lookup"><span data-stu-id="26316-132">Continue without prompts</span></span>

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

### <span data-ttu-id="26316-133">-MaximumNodeCount</span><span class="sxs-lookup"><span data-stu-id="26316-133">-MaximumNodeCount</span></span>
<span data-ttu-id="26316-134">애플리케이션을 두는 최대 노드 수를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="26316-134">Specifies the maximum number of nodes on which to place an application</span></span>

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

### <span data-ttu-id="26316-135">-MinimumNodeCount</span><span class="sxs-lookup"><span data-stu-id="26316-135">-MinimumNodeCount</span></span>
<span data-ttu-id="26316-136">Service Fabric이 이 애플리케이션에 대한 용량을 예약할 노드의 최소 수를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="26316-136">Specifies the minimum number of nodes where Service Fabric will reserve capacity for this application</span></span>

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

### <span data-ttu-id="26316-137">-Name</span><span class="sxs-lookup"><span data-stu-id="26316-137">-Name</span></span>
<span data-ttu-id="26316-138">애플리케이션 이름 지정</span><span class="sxs-lookup"><span data-stu-id="26316-138">Specify the name of the application</span></span>

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

### <span data-ttu-id="26316-139">-PackageUrl</span><span class="sxs-lookup"><span data-stu-id="26316-139">-PackageUrl</span></span>
<span data-ttu-id="26316-140">애플리케이션 패키지 sfpkg 파일의 URL 지정</span><span class="sxs-lookup"><span data-stu-id="26316-140">Specify the url of the application package sfpkg file</span></span>

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

### <span data-ttu-id="26316-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="26316-141">-ResourceGroupName</span></span>
<span data-ttu-id="26316-142">리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="26316-142">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="26316-143">-확인</span><span class="sxs-lookup"><span data-stu-id="26316-143">-Confirm</span></span>
<span data-ttu-id="26316-144">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="26316-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="26316-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="26316-145">-WhatIf</span></span>
<span data-ttu-id="26316-146">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="26316-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="26316-147">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="26316-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="26316-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26316-148">CommonParameters</span></span>
<span data-ttu-id="26316-149">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="26316-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26316-150">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="26316-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26316-151">입력</span><span class="sxs-lookup"><span data-stu-id="26316-151">INPUTS</span></span>

### <span data-ttu-id="26316-152">System.String</span><span class="sxs-lookup"><span data-stu-id="26316-152">System.String</span></span>

### <span data-ttu-id="26316-153">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="26316-153">System.Collections.Hashtable</span></span>

## <span data-ttu-id="26316-154">출력</span><span class="sxs-lookup"><span data-stu-id="26316-154">OUTPUTS</span></span>

### <span data-ttu-id="26316-155">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplication</span><span class="sxs-lookup"><span data-stu-id="26316-155">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplication</span></span>

## <span data-ttu-id="26316-156">참고 사항</span><span class="sxs-lookup"><span data-stu-id="26316-156">NOTES</span></span>

## <span data-ttu-id="26316-157">관련 링크</span><span class="sxs-lookup"><span data-stu-id="26316-157">RELATED LINKS</span></span>
