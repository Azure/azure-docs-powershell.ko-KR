---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/remove-azservicefabricapplicationtypeversion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricApplicationTypeVersion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricApplicationTypeVersion.md
ms.openlocfilehash: 498dec77dfc2f4ede8ae81aa70b10acfe2ad2954
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94056987"
---
# <span data-ttu-id="8adea-101">Remove-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="8adea-101">Remove-AzServiceFabricApplicationTypeVersion</span></span>

## <span data-ttu-id="8adea-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8adea-102">SYNOPSIS</span></span>
<span data-ttu-id="8adea-103">서비스 패브릭 제거 클러스터의 응용 프로그램 유형 버전입니다.</span><span class="sxs-lookup"><span data-stu-id="8adea-103">Remove Service fabric an application type version from the cluster.</span></span>

## <span data-ttu-id="8adea-104">구문과</span><span class="sxs-lookup"><span data-stu-id="8adea-104">SYNTAX</span></span>

### <span data-ttu-id="8adea-105">ByResourceGroup (기본값)</span><span class="sxs-lookup"><span data-stu-id="8adea-105">ByResourceGroup (Default)</span></span>
```
Remove-AzServiceFabricApplicationTypeVersion [-ResourceGroupName] <String> [-ClusterName] <String>
 -Name <String> -Version <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8adea-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="8adea-106">ByResourceId</span></span>
```
Remove-AzServiceFabricApplicationTypeVersion -ResourceId <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8adea-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="8adea-107">ByInputObject</span></span>
```
Remove-AzServiceFabricApplicationTypeVersion -InputObject <PSApplicationTypeVersion> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8adea-108">설명은</span><span class="sxs-lookup"><span data-stu-id="8adea-108">DESCRIPTION</span></span>
<span data-ttu-id="8adea-109">이 cmdlet은 클러스터에서 서비스 패브릭을 응용 프로그램 유형 버전으로 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="8adea-109">This cmdlet will remove Service fabric an application type version from the cluster.</span></span> <span data-ttu-id="8adea-110">이 명령을 실행 하기 전에이 리소스의 모든 응용 프로그램을 제거 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="8adea-110">All applications under this resource must be removed before running this command.</span></span>

## <span data-ttu-id="8adea-111">예제의</span><span class="sxs-lookup"><span data-stu-id="8adea-111">EXAMPLES</span></span>

### <span data-ttu-id="8adea-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="8adea-112">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appTypeName = "testAppType"
PS C:\> $version = "v1"
PS C:\> Remove-AzServiceFabricApplicationTypeVersion -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appTypeName -Version $version -Force -PassThru -Verbose
```

<span data-ttu-id="8adea-113">이 예제에서는 "testAppType" 형식 아래의 버전 "v1"을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="8adea-113">This example will remove the version "v1" under the type "testAppType".</span></span> <span data-ttu-id="8adea-114">이 리소스에는 모든 응용 프로그램이 있으므로 명령에서 예외를 throw 합니다.</span><span class="sxs-lookup"><span data-stu-id="8adea-114">It there are any applications under this resource the command will throw an exception.</span></span>

## <span data-ttu-id="8adea-115">변수</span><span class="sxs-lookup"><span data-stu-id="8adea-115">PARAMETERS</span></span>

### <span data-ttu-id="8adea-116">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="8adea-116">-ClusterName</span></span>
<span data-ttu-id="8adea-117">클러스터의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8adea-117">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="8adea-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8adea-118">-DefaultProfile</span></span>
<span data-ttu-id="8adea-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="8adea-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8adea-120">-Force</span><span class="sxs-lookup"><span data-stu-id="8adea-120">-Force</span></span>
<span data-ttu-id="8adea-121">메시지를 표시 하지 않고 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="8adea-121">Remove without prompt.</span></span>

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

### <span data-ttu-id="8adea-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8adea-122">-InputObject</span></span>
<span data-ttu-id="8adea-123">응용 프로그램 종류 버전 리소스입니다.</span><span class="sxs-lookup"><span data-stu-id="8adea-123">The application type version resource.</span></span>

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

### <span data-ttu-id="8adea-124">-이름</span><span class="sxs-lookup"><span data-stu-id="8adea-124">-Name</span></span>
<span data-ttu-id="8adea-125">응용 프로그램 종류의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8adea-125">Specify the name of the application type.</span></span>

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

### <span data-ttu-id="8adea-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8adea-126">-PassThru</span></span>
<span data-ttu-id="8adea-127">{{Fill PassThru 설명}}</span><span class="sxs-lookup"><span data-stu-id="8adea-127">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="8adea-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8adea-128">-ResourceGroupName</span></span>
<span data-ttu-id="8adea-129">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8adea-129">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="8adea-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8adea-130">-ResourceId</span></span>
<span data-ttu-id="8adea-131">응용 프로그램 유형 버전의 팔 ResourceId입니다.</span><span class="sxs-lookup"><span data-stu-id="8adea-131">Arm ResourceId of the application type version.</span></span>

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

### <span data-ttu-id="8adea-132">-버전</span><span class="sxs-lookup"><span data-stu-id="8adea-132">-Version</span></span>
<span data-ttu-id="8adea-133">응용 프로그램 종류 버전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8adea-133">Specify the application type version.</span></span>

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

### <span data-ttu-id="8adea-134">-확인</span><span class="sxs-lookup"><span data-stu-id="8adea-134">-Confirm</span></span>
<span data-ttu-id="8adea-135">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="8adea-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8adea-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8adea-136">-WhatIf</span></span>
<span data-ttu-id="8adea-137">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="8adea-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8adea-138">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="8adea-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8adea-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8adea-139">CommonParameters</span></span>
<span data-ttu-id="8adea-140">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="8adea-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8adea-141">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="8adea-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8adea-142">입력</span><span class="sxs-lookup"><span data-stu-id="8adea-142">INPUTS</span></span>

### <span data-ttu-id="8adea-143">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="8adea-143">System.String</span></span>

### <span data-ttu-id="8adea-144">ServiceFabric. m i m a.</span><span class="sxs-lookup"><span data-stu-id="8adea-144">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplicationTypeVersion</span></span>

## <span data-ttu-id="8adea-145">출력</span><span class="sxs-lookup"><span data-stu-id="8adea-145">OUTPUTS</span></span>

### <span data-ttu-id="8adea-146">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="8adea-146">System.Boolean</span></span>

## <span data-ttu-id="8adea-147">상속자</span><span class="sxs-lookup"><span data-stu-id="8adea-147">NOTES</span></span>

## <span data-ttu-id="8adea-148">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8adea-148">RELATED LINKS</span></span>
