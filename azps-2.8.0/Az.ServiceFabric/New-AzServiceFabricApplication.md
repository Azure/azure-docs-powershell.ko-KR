---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/new-azservicefabricapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/New-AzServiceFabricApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/New-AzServiceFabricApplication.md
ms.openlocfilehash: 7a337ed6e347d5ab22cd04baac2acb1c7e0b171d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93873058"
---
# <span data-ttu-id="2f8a2-101">New-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="2f8a2-101">New-AzServiceFabricApplication</span></span>

## <span data-ttu-id="2f8a2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2f8a2-102">SYNOPSIS</span></span>
<span data-ttu-id="2f8a2-103">지정 된 리소스 그룹 및 클러스터 아래에 새 service fabric 응용 프로그램을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="2f8a2-103">Create new service fabric application under the specified resource group and cluster.</span></span>

## <span data-ttu-id="2f8a2-104">구문과</span><span class="sxs-lookup"><span data-stu-id="2f8a2-104">SYNTAX</span></span>

### <span data-ttu-id="2f8a2-105">SkipAppTypeVersion (기본값)</span><span class="sxs-lookup"><span data-stu-id="2f8a2-105">SkipAppTypeVersion (Default)</span></span>
```
New-AzServiceFabricApplication [-ResourceGroupName] <String> [-ClusterName] <String>
 [-ApplicationTypeName] <String> [-ApplicationTypeVersion] <String> -Name <String>
 [-ApplicationParameter <Hashtable>] [-MinimumNodeCount <Int64>] [-MaximumNodeCount <Int64>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2f8a2-106">CreateAppTypeVersion</span><span class="sxs-lookup"><span data-stu-id="2f8a2-106">CreateAppTypeVersion</span></span>
```
New-AzServiceFabricApplication [-ResourceGroupName] <String> [-ClusterName] <String>
 [-ApplicationTypeName] <String> [-ApplicationTypeVersion] <String> -Name <String>
 [-ApplicationParameter <Hashtable>] -PackageUrl <String> [-MinimumNodeCount <Int64>]
 [-MaximumNodeCount <Int64>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2f8a2-107">설명은</span><span class="sxs-lookup"><span data-stu-id="2f8a2-107">DESCRIPTION</span></span>
<span data-ttu-id="2f8a2-108">이 cmdlet은 지정 된 리소스 그룹 및 클러스터 아래에 새 서비스 패브릭 응용 프로그램을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="2f8a2-108">This cmdlet creates a new service fabric application under the specified resource group and cluster.</span></span> <span data-ttu-id="2f8a2-109">매개 변수-PackageUrl을 사용 하 여 형식 버전을 만들 수 있지만, 형식이 ' 실패 ' 상태 이면 사용자가 형식 버전을 다시 만들지 여부를 cmdlet에서 묻는 메시지가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="2f8a2-109">The parameter -PackageUrl can be used to create the type version, If the type version already exits but its in 'Failed' state the cmdlet will ask if the user wants to recreate the type version.</span></span> <span data-ttu-id="2f8a2-110">' 실패 ' 상태가 계속 되 면 명령이 프로세스를 중지 하 고 예외를 발생 시킵니다.</span><span class="sxs-lookup"><span data-stu-id="2f8a2-110">If it continues in 'Failed' state, the command will stop the process and throw an exception.</span></span>

## <span data-ttu-id="2f8a2-111">예제의</span><span class="sxs-lookup"><span data-stu-id="2f8a2-111">EXAMPLES</span></span>

### <span data-ttu-id="2f8a2-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="2f8a2-112">Example 1</span></span>
```powershell
PS C:\> New-AzServiceFabricApplication -ResourceGroupName "testRG" -ClusterName "testCluster" -ApplicationTypeName "TestAppType" -ApplicationTypeVersion "v1" -Name "testApp" -ApplicationParameter @{key0="value0";key1=$null;key2="value2"}
```

<span data-ttu-id="2f8a2-113">이 예제에서는 리소스 그룹 "testRG" 및 클러스터 "testCluster"에 "testApp" 응용 프로그램을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="2f8a2-113">This example creates the application "testApp" under resource group "testRG" and cluster "testCluster".</span></span> <span data-ttu-id="2f8a2-114">"TestAppType" 버전 "v1" 응용 프로그램 종류는 클러스터에 이미 있어야 하 고, 응용 프로그램 매개 변수는 응용 프로그램 매니페스트에서 정의 되어야 하며, 그렇지 않으면 cmdlet이 실패 합니다.</span><span class="sxs-lookup"><span data-stu-id="2f8a2-114">The application type "TestAppType" version "v1" should already exist in the cluster, and the application parameters should be defined in the application manifest otherwise the cmdlet will fail.</span></span>

### <span data-ttu-id="2f8a2-115">예제 2: 응용 프로그램을 만들기 전에 응용 프로그램 종류 버전을 만들기 위한-PackageUrl을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2f8a2-115">Example 2: Specify -PackageUrl to create the application type version before creating the application.</span></span>
```powershell
PS C:\> New-AzServiceFabricApplication -ResourceGroupName "testRG" -ClusterName "testCluster" -ApplicationTypeName "TestAppType" -ApplicationTypeVersion "v1" -Name "testApp" -PackageUrl "https://sftestapp.blob.core.windows.net/sftestapp/testApp_1.0.sfpkg" -ApplicationParameter @{key0="value0";key1=$null;key2="value2"}
```

<span data-ttu-id="2f8a2-116">이 예제에서는 제공 된 패키지 url을 사용 하 여 응용 프로그램 유형 "TestAppType" 버전 "v1"을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="2f8a2-116">This example creates the application type "TestAppType"  version "v1" using the package url provided.</span></span> <span data-ttu-id="2f8a2-117">그 후에는 일반적인 프로세스를 계속 하 여 응용 프로그램을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="2f8a2-117">After this, it will continue the normal process to create the application.</span></span> <span data-ttu-id="2f8a2-118">응용 프로그램 유형 버전이 이미 종료 되 고 프로 비전 상태가 ' 실패 ' 인 경우 사용자가 형식 버전을 다시 만들지 여부를 확인 하는 메시지가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="2f8a2-118">If the application type version already exits and the provisioning state its in 'Failed' it will prompt to decide if the user wants to recreate the type version.</span></span>

## <span data-ttu-id="2f8a2-119">변수</span><span class="sxs-lookup"><span data-stu-id="2f8a2-119">PARAMETERS</span></span>

### <span data-ttu-id="2f8a2-120">-ApplicationParameter</span><span class="sxs-lookup"><span data-stu-id="2f8a2-120">-ApplicationParameter</span></span>
<span data-ttu-id="2f8a2-121">응용 프로그램 매개 변수를 키/값 쌍으로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2f8a2-121">Specify the application parameters as key/value pairs.</span></span>
<span data-ttu-id="2f8a2-122">이러한 매개 변수는 응용 프로그램 매니페스트에 존재 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="2f8a2-122">These parameters must exist in the application manifest.</span></span>

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

### <span data-ttu-id="2f8a2-123">-ApplicationTypeName</span><span class="sxs-lookup"><span data-stu-id="2f8a2-123">-ApplicationTypeName</span></span>
<span data-ttu-id="2f8a2-124">응용 프로그램 종류의 이름 지정</span><span class="sxs-lookup"><span data-stu-id="2f8a2-124">Specify the name of the application type</span></span>

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

### <span data-ttu-id="2f8a2-125">-ApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="2f8a2-125">-ApplicationTypeVersion</span></span>
<span data-ttu-id="2f8a2-126">응용 프로그램 종류 버전 지정</span><span class="sxs-lookup"><span data-stu-id="2f8a2-126">Specify the application type version</span></span>

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

### <span data-ttu-id="2f8a2-127">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="2f8a2-127">-ClusterName</span></span>
<span data-ttu-id="2f8a2-128">클러스터의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2f8a2-128">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="2f8a2-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2f8a2-129">-DefaultProfile</span></span>
<span data-ttu-id="2f8a2-130">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="2f8a2-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2f8a2-131">-Force</span><span class="sxs-lookup"><span data-stu-id="2f8a2-131">-Force</span></span>
<span data-ttu-id="2f8a2-132">메시지 없이 계속</span><span class="sxs-lookup"><span data-stu-id="2f8a2-132">Continue without prompts</span></span>

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

### <span data-ttu-id="2f8a2-133">-MaximumNodeCount</span><span class="sxs-lookup"><span data-stu-id="2f8a2-133">-MaximumNodeCount</span></span>
<span data-ttu-id="2f8a2-134">응용 프로그램을 배치할 최대 노드 수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2f8a2-134">Specifies the maximum number of nodes on which to place an application</span></span>

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

### <span data-ttu-id="2f8a2-135">-MinimumNodeCount</span><span class="sxs-lookup"><span data-stu-id="2f8a2-135">-MinimumNodeCount</span></span>
<span data-ttu-id="2f8a2-136">서비스 패브릭에서이 응용 프로그램에 대 한 용량을 예약할 최소 노드 수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2f8a2-136">Specifies the minimum number of nodes where Service Fabric will reserve capacity for this application</span></span>

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

### <span data-ttu-id="2f8a2-137">-이름</span><span class="sxs-lookup"><span data-stu-id="2f8a2-137">-Name</span></span>
<span data-ttu-id="2f8a2-138">응용 프로그램 이름 지정</span><span class="sxs-lookup"><span data-stu-id="2f8a2-138">Specify the name of the application</span></span>

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

### <span data-ttu-id="2f8a2-139">-PackageUrl</span><span class="sxs-lookup"><span data-stu-id="2f8a2-139">-PackageUrl</span></span>
<span data-ttu-id="2f8a2-140">응용 프로그램 패키지 sfpkg 파일의 url을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2f8a2-140">Specify the url of the application package sfpkg file</span></span>

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

### <span data-ttu-id="2f8a2-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2f8a2-141">-ResourceGroupName</span></span>
<span data-ttu-id="2f8a2-142">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2f8a2-142">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="2f8a2-143">-확인</span><span class="sxs-lookup"><span data-stu-id="2f8a2-143">-Confirm</span></span>
<span data-ttu-id="2f8a2-144">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="2f8a2-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2f8a2-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2f8a2-145">-WhatIf</span></span>
<span data-ttu-id="2f8a2-146">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="2f8a2-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2f8a2-147">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2f8a2-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2f8a2-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f8a2-148">CommonParameters</span></span>
<span data-ttu-id="2f8a2-149">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="2f8a2-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f8a2-150">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2f8a2-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f8a2-151">입력</span><span class="sxs-lookup"><span data-stu-id="2f8a2-151">INPUTS</span></span>

### <span data-ttu-id="2f8a2-152">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="2f8a2-152">System.String</span></span>

### <span data-ttu-id="2f8a2-153">System.webserver. 컬렉션 테이블</span><span class="sxs-lookup"><span data-stu-id="2f8a2-153">System.Collections.Hashtable</span></span>

## <span data-ttu-id="2f8a2-154">출력</span><span class="sxs-lookup"><span data-stu-id="2f8a2-154">OUTPUTS</span></span>

### <span data-ttu-id="2f8a2-155">ServiceFabric 응용 프로그램의 경우</span><span class="sxs-lookup"><span data-stu-id="2f8a2-155">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplication</span></span>

## <span data-ttu-id="2f8a2-156">상속자</span><span class="sxs-lookup"><span data-stu-id="2f8a2-156">NOTES</span></span>

## <span data-ttu-id="2f8a2-157">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2f8a2-157">RELATED LINKS</span></span>
