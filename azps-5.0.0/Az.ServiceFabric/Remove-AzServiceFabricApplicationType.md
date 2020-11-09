---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/remove-azservicefabricapplicationtype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricApplicationType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricApplicationType.md
ms.openlocfilehash: 87557a67c8cb087b8a22ecc9cdfa59a3690057dc
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94304505"
---
# <span data-ttu-id="a27c8-101">Remove-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="a27c8-101">Remove-AzServiceFabricApplicationType</span></span>

## <span data-ttu-id="a27c8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a27c8-102">SYNOPSIS</span></span>
<span data-ttu-id="a27c8-103">서비스 패브릭 제거 클러스터의 응용 프로그램 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="a27c8-103">Remove Service fabric an application type from the cluster.</span></span> <span data-ttu-id="a27c8-104">이 리소스 아래에 모든 유형의 버전이 제거 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a27c8-104">This will remove all type versions under this resource.</span></span>

## <span data-ttu-id="a27c8-105">구문과</span><span class="sxs-lookup"><span data-stu-id="a27c8-105">SYNTAX</span></span>

### <span data-ttu-id="a27c8-106">ByResourceGroup (기본값)</span><span class="sxs-lookup"><span data-stu-id="a27c8-106">ByResourceGroup (Default)</span></span>
```
Remove-AzServiceFabricApplicationType [-ResourceGroupName] <String> [-ClusterName] <String> [-Name <String>]
 [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a27c8-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="a27c8-107">ByResourceId</span></span>
```
Remove-AzServiceFabricApplicationType -ResourceId <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a27c8-108">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="a27c8-108">ByInputObject</span></span>
```
Remove-AzServiceFabricApplicationType -InputObject <PSApplicationType> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a27c8-109">설명은</span><span class="sxs-lookup"><span data-stu-id="a27c8-109">DESCRIPTION</span></span>
<span data-ttu-id="a27c8-110">이 cmdlet은 클러스터에서 응용 프로그램 종류를 제거 하 고이 리소스의 모든 형식 버전을 제거 하지만, 그 아래에 있는 모든 응용 프로그램은이 명령을 실행 하기 전에 제거 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a27c8-110">This cmdlet removes an application type form the cluster and will remove all type version under this resource, but all applications under it should be removed before running this command.</span></span>

## <span data-ttu-id="a27c8-111">예제의</span><span class="sxs-lookup"><span data-stu-id="a27c8-111">EXAMPLES</span></span>

### <span data-ttu-id="a27c8-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="a27c8-112">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appTypeName = "testAppType"
PS C:\> Remove-AzServiceFabricApplicationType -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appTypeName -Verbose
```

<span data-ttu-id="a27c8-113">이 예제에서는 응용 프로그램 유형 "testAppType" 및 그 아래에 있는 모든 버전을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="a27c8-113">This example will remove the application type "testAppType" and all the version under it.</span></span> <span data-ttu-id="a27c8-114">이 형식으로 만든 응용 프로그램이 있는 경우 명령에서 예외를 throw 합니다.</span><span class="sxs-lookup"><span data-stu-id="a27c8-114">If there are any applications created with this type, the command will throw an exception.</span></span>

## <span data-ttu-id="a27c8-115">변수</span><span class="sxs-lookup"><span data-stu-id="a27c8-115">PARAMETERS</span></span>

### <span data-ttu-id="a27c8-116">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="a27c8-116">-ClusterName</span></span>
<span data-ttu-id="a27c8-117">클러스터의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a27c8-117">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="a27c8-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a27c8-118">-DefaultProfile</span></span>
<span data-ttu-id="a27c8-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a27c8-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a27c8-120">-Force</span><span class="sxs-lookup"><span data-stu-id="a27c8-120">-Force</span></span>
<span data-ttu-id="a27c8-121">메시지를 표시 하지 않고 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="a27c8-121">Remove without prompt.</span></span>

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

### <span data-ttu-id="a27c8-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a27c8-122">-InputObject</span></span>
<span data-ttu-id="a27c8-123">응용 프로그램 종류 리소스입니다.</span><span class="sxs-lookup"><span data-stu-id="a27c8-123">The application type resource.</span></span>

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

### <span data-ttu-id="a27c8-124">-이름</span><span class="sxs-lookup"><span data-stu-id="a27c8-124">-Name</span></span>
<span data-ttu-id="a27c8-125">응용 프로그램 종류의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a27c8-125">Specify the name of the application type.</span></span>

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

### <span data-ttu-id="a27c8-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a27c8-126">-PassThru</span></span>
<span data-ttu-id="a27c8-127">{{Fill PassThru 설명}}</span><span class="sxs-lookup"><span data-stu-id="a27c8-127">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="a27c8-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a27c8-128">-ResourceGroupName</span></span>
<span data-ttu-id="a27c8-129">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a27c8-129">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="a27c8-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a27c8-130">-ResourceId</span></span>
<span data-ttu-id="a27c8-131">응용 프로그램 종류의 팔 ResourceId입니다.</span><span class="sxs-lookup"><span data-stu-id="a27c8-131">Arm ResourceId of the application type.</span></span>

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

### <span data-ttu-id="a27c8-132">-확인</span><span class="sxs-lookup"><span data-stu-id="a27c8-132">-Confirm</span></span>
<span data-ttu-id="a27c8-133">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="a27c8-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a27c8-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a27c8-134">-WhatIf</span></span>
<span data-ttu-id="a27c8-135">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="a27c8-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a27c8-136">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a27c8-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a27c8-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a27c8-137">CommonParameters</span></span>
<span data-ttu-id="a27c8-138">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a27c8-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a27c8-139">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="a27c8-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a27c8-140">입력</span><span class="sxs-lookup"><span data-stu-id="a27c8-140">INPUTS</span></span>

### <span data-ttu-id="a27c8-141">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="a27c8-141">System.String</span></span>

### <span data-ttu-id="a27c8-142">ServiceFabric. m a m/. m i m m Applicationtype</span><span class="sxs-lookup"><span data-stu-id="a27c8-142">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplicationType</span></span>

## <span data-ttu-id="a27c8-143">출력</span><span class="sxs-lookup"><span data-stu-id="a27c8-143">OUTPUTS</span></span>

### <span data-ttu-id="a27c8-144">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="a27c8-144">System.Boolean</span></span>

## <span data-ttu-id="a27c8-145">상속자</span><span class="sxs-lookup"><span data-stu-id="a27c8-145">NOTES</span></span>

## <span data-ttu-id="a27c8-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a27c8-146">RELATED LINKS</span></span>
