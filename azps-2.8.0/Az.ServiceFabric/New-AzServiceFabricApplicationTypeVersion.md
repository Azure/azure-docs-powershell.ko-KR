---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/new-azservicefabricapplicationtypeversion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/New-AzServiceFabricApplicationTypeVersion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/New-AzServiceFabricApplicationTypeVersion.md
ms.openlocfilehash: 69fa98b75b6897355b34ba91a39196f072d6af6a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93873057"
---
# <span data-ttu-id="ba02d-101">New-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="ba02d-101">New-AzServiceFabricApplicationTypeVersion</span></span>

## <span data-ttu-id="ba02d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ba02d-102">SYNOPSIS</span></span>
<span data-ttu-id="ba02d-103">지정 된 리소스 그룹 및 클러스터 아래에 새 응용 프로그램 종류 버전을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ba02d-103">Create new application type version under the specified resource group and cluster.</span></span>

## <span data-ttu-id="ba02d-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ba02d-104">SYNTAX</span></span>

```
New-AzServiceFabricApplicationTypeVersion [-ResourceGroupName] <String> [-ClusterName] <String>
 [-Name] <String> [-Version] <String> -PackageUrl <String> [-DefaultParameter <Hashtable>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ba02d-105">설명은</span><span class="sxs-lookup"><span data-stu-id="ba02d-105">DESCRIPTION</span></span>
<span data-ttu-id="ba02d-106">이 cmdlet은-PackageUrl에 지정 된 패키지를 사용 하 여 새 응용 프로그램 유형 버전을 만들며, 배포 중에 Azure 리소스 관리자가 사용할 REST 끝점을 통해 액세스할 수 있어야 하며 sfpkg를 사용 하 여 패키지 및 압축 된 응용 프로그램을 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba02d-106">This cmdlet creates a new application type version using the package specified in -PackageUrl, this should be accessible through a REST endpoint for Azure Resource Manager to consume during deployment and contained The application packaged and zipped with the extension .sfpkg.</span></span> <span data-ttu-id="ba02d-107">이 명령은 아직 없는 경우 응용 프로그램 종류를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ba02d-107">This command will create the application type if it doesn't exist already.</span></span>

## <span data-ttu-id="ba02d-108">예제의</span><span class="sxs-lookup"><span data-stu-id="ba02d-108">EXAMPLES</span></span>

### <span data-ttu-id="ba02d-109">예제 1</span><span class="sxs-lookup"><span data-stu-id="ba02d-109">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appTypeName = "testAppType"
PS C:\> $version = "v1"
PS C:\> $packageUrl = "https://sftestapp.blob.core.windows.net/sftestapp/testApp_1.0.sfpkg"
PS C:\> New-AzServiceFabricApplicationTypeVersion -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appTypeName -Version $version -PackageUrl $packageUrl -Verbose
```

<span data-ttu-id="ba02d-110">이 예제에서는 "testAppType" 형식으로 응용 프로그램 유형 버전 "v1"을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ba02d-110">This example will create an application type version "v1" under type "testAppType".</span></span> <span data-ttu-id="ba02d-111">패키지에 포함 된 응용 프로그램 매니페스트의 버전은 버전에 지정 된 것과 동일한 버전을 사용 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba02d-111">The version in the application manifest contained in the package should have the same version as the one specified in -Version.</span></span>

## <span data-ttu-id="ba02d-112">변수</span><span class="sxs-lookup"><span data-stu-id="ba02d-112">PARAMETERS</span></span>

### <span data-ttu-id="ba02d-113">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="ba02d-113">-ClusterName</span></span>
<span data-ttu-id="ba02d-114">클러스터의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba02d-114">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="ba02d-115">-DefaultParameter</span><span class="sxs-lookup"><span data-stu-id="ba02d-115">-DefaultParameter</span></span>
<span data-ttu-id="ba02d-116">응용 프로그램 매개 변수의 기본 값을 키/값 쌍으로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba02d-116">Specify the default values of the application parameters as key/value pairs.</span></span>
<span data-ttu-id="ba02d-117">이러한 매개 변수는 응용 프로그램 매니페스트에 존재 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba02d-117">These parameters must exist in the application manifest.</span></span>

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

### <span data-ttu-id="ba02d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba02d-118">-DefaultProfile</span></span>
<span data-ttu-id="ba02d-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ba02d-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ba02d-120">-Force</span><span class="sxs-lookup"><span data-stu-id="ba02d-120">-Force</span></span>
<span data-ttu-id="ba02d-121">메시지 없이 계속</span><span class="sxs-lookup"><span data-stu-id="ba02d-121">Continue without prompts</span></span>

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

### <span data-ttu-id="ba02d-122">-이름</span><span class="sxs-lookup"><span data-stu-id="ba02d-122">-Name</span></span>
<span data-ttu-id="ba02d-123">응용 프로그램 종류의 이름 지정</span><span class="sxs-lookup"><span data-stu-id="ba02d-123">Specify the name of the application type</span></span>

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

### <span data-ttu-id="ba02d-124">-PackageUrl</span><span class="sxs-lookup"><span data-stu-id="ba02d-124">-PackageUrl</span></span>
<span data-ttu-id="ba02d-125">응용 프로그램 패키지 sfpkg 파일의 url을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba02d-125">Specify the url of the application package sfpkg file</span></span>

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

### <span data-ttu-id="ba02d-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ba02d-126">-ResourceGroupName</span></span>
<span data-ttu-id="ba02d-127">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba02d-127">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="ba02d-128">-버전</span><span class="sxs-lookup"><span data-stu-id="ba02d-128">-Version</span></span>
<span data-ttu-id="ba02d-129">응용 프로그램 종류 버전 지정</span><span class="sxs-lookup"><span data-stu-id="ba02d-129">Specify the application type version</span></span>

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

### <span data-ttu-id="ba02d-130">-확인</span><span class="sxs-lookup"><span data-stu-id="ba02d-130">-Confirm</span></span>
<span data-ttu-id="ba02d-131">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba02d-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ba02d-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ba02d-132">-WhatIf</span></span>
<span data-ttu-id="ba02d-133">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="ba02d-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ba02d-134">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ba02d-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ba02d-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba02d-135">CommonParameters</span></span>
<span data-ttu-id="ba02d-136">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba02d-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba02d-137">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ba02d-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba02d-138">입력</span><span class="sxs-lookup"><span data-stu-id="ba02d-138">INPUTS</span></span>

### <span data-ttu-id="ba02d-139">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="ba02d-139">System.String</span></span>

### <span data-ttu-id="ba02d-140">System.webserver. 컬렉션 테이블</span><span class="sxs-lookup"><span data-stu-id="ba02d-140">System.Collections.Hashtable</span></span>

## <span data-ttu-id="ba02d-141">출력</span><span class="sxs-lookup"><span data-stu-id="ba02d-141">OUTPUTS</span></span>

### <span data-ttu-id="ba02d-142">ServiceFabric. m i m a.</span><span class="sxs-lookup"><span data-stu-id="ba02d-142">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplicationTypeVersion</span></span>

## <span data-ttu-id="ba02d-143">상속자</span><span class="sxs-lookup"><span data-stu-id="ba02d-143">NOTES</span></span>

## <span data-ttu-id="ba02d-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ba02d-144">RELATED LINKS</span></span>
