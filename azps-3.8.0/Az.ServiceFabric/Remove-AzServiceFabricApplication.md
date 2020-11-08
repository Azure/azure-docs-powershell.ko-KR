---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/remove-azservicefabricapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricApplication.md
ms.openlocfilehash: e9f248575d0f5193a11c729384e674870b3de29c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94041692"
---
# <span data-ttu-id="c7888-101">Remove-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="c7888-101">Remove-AzServiceFabricApplication</span></span>

## <span data-ttu-id="c7888-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c7888-102">SYNOPSIS</span></span>
<span data-ttu-id="c7888-103">클러스터에서 응용 프로그램을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="c7888-103">Remove an application from the cluster.</span></span> <span data-ttu-id="c7888-104">이렇게 하면 응용 프로그램 아래에 있는 서비스가 모두 제거 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c7888-104">This will remove all the services under the application.</span></span>

## <span data-ttu-id="c7888-105">구문과</span><span class="sxs-lookup"><span data-stu-id="c7888-105">SYNTAX</span></span>

### <span data-ttu-id="c7888-106">ByResourceGroup (기본값)</span><span class="sxs-lookup"><span data-stu-id="c7888-106">ByResourceGroup (Default)</span></span>
```
Remove-AzServiceFabricApplication [-ResourceGroupName] <String> [-ClusterName] <String> [-Name] <String>
 [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c7888-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="c7888-107">ByResourceId</span></span>
```
Remove-AzServiceFabricApplication -ResourceId <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c7888-108">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="c7888-108">ByInputObject</span></span>
```
Remove-AzServiceFabricApplication -InputObject <PSApplication> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c7888-109">설명은</span><span class="sxs-lookup"><span data-stu-id="c7888-109">DESCRIPTION</span></span>
<span data-ttu-id="c7888-110">이 cmdlet은 클러스터를 구성 하는 응용 프로그램을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="c7888-110">This cmdlet removes an application form the cluster.</span></span> <span data-ttu-id="c7888-111">이렇게 하면 응용 프로그램 리소스 아래에 모든 서비스가 제거 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c7888-111">This will remove all the services, if any, under the application resource.</span></span>

## <span data-ttu-id="c7888-112">예제의</span><span class="sxs-lookup"><span data-stu-id="c7888-112">EXAMPLES</span></span>

### <span data-ttu-id="c7888-113">예제 1</span><span class="sxs-lookup"><span data-stu-id="c7888-113">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appName = "testApp"
PS C:\> Remove-AzServiceFabricApplication -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appName
```

<span data-ttu-id="c7888-114">이 예제에서는 리소스 그룹 "testRG" 및 클러스터 "testCluster" 아래에서 "testApp" 응용 프로그램을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="c7888-114">This example removes the application "testApp" under the resource group "testRG" and cluster "testCluster".</span></span>

## <span data-ttu-id="c7888-115">변수</span><span class="sxs-lookup"><span data-stu-id="c7888-115">PARAMETERS</span></span>

### <span data-ttu-id="c7888-116">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="c7888-116">-ClusterName</span></span>
<span data-ttu-id="c7888-117">클러스터의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c7888-117">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="c7888-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c7888-118">-DefaultProfile</span></span>
<span data-ttu-id="c7888-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c7888-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c7888-120">-Force</span><span class="sxs-lookup"><span data-stu-id="c7888-120">-Force</span></span>
<span data-ttu-id="c7888-121">메시지를 표시 하지 않고 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="c7888-121">Remove without prompt.</span></span>

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

### <span data-ttu-id="c7888-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c7888-122">-InputObject</span></span>
<span data-ttu-id="c7888-123">응용 프로그램 리소스.</span><span class="sxs-lookup"><span data-stu-id="c7888-123">The application resource.</span></span>

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

### <span data-ttu-id="c7888-124">-이름</span><span class="sxs-lookup"><span data-stu-id="c7888-124">-Name</span></span>
<span data-ttu-id="c7888-125">응용 프로그램의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c7888-125">Specify the name of the application.</span></span>

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

### <span data-ttu-id="c7888-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c7888-126">-PassThru</span></span>
<span data-ttu-id="c7888-127">{{Fill PassThru 설명}}</span><span class="sxs-lookup"><span data-stu-id="c7888-127">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="c7888-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c7888-128">-ResourceGroupName</span></span>
<span data-ttu-id="c7888-129">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c7888-129">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="c7888-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c7888-130">-ResourceId</span></span>
<span data-ttu-id="c7888-131">응용 프로그램의 팔 ResourceId입니다.</span><span class="sxs-lookup"><span data-stu-id="c7888-131">Arm ResourceId of the application.</span></span>

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

### <span data-ttu-id="c7888-132">-확인</span><span class="sxs-lookup"><span data-stu-id="c7888-132">-Confirm</span></span>
<span data-ttu-id="c7888-133">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="c7888-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c7888-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c7888-134">-WhatIf</span></span>
<span data-ttu-id="c7888-135">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="c7888-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c7888-136">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c7888-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c7888-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7888-137">CommonParameters</span></span>
<span data-ttu-id="c7888-138">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c7888-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7888-139">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c7888-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7888-140">입력</span><span class="sxs-lookup"><span data-stu-id="c7888-140">INPUTS</span></span>

### <span data-ttu-id="c7888-141">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="c7888-141">System.String</span></span>

### <span data-ttu-id="c7888-142">ServiceFabric 응용 프로그램의 경우</span><span class="sxs-lookup"><span data-stu-id="c7888-142">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplication</span></span>

## <span data-ttu-id="c7888-143">출력</span><span class="sxs-lookup"><span data-stu-id="c7888-143">OUTPUTS</span></span>

### <span data-ttu-id="c7888-144">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="c7888-144">System.Boolean</span></span>

## <span data-ttu-id="c7888-145">상속자</span><span class="sxs-lookup"><span data-stu-id="c7888-145">NOTES</span></span>

## <span data-ttu-id="c7888-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c7888-146">RELATED LINKS</span></span>
