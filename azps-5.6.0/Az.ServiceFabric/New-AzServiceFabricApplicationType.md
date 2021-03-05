---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/powershell/module/az.servicefabric/new-azservicefabricapplicationtype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/New-AzServiceFabricApplicationType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/New-AzServiceFabricApplicationType.md
ms.openlocfilehash: f8724fe13cb44ac3e2640f747026c121303be252
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101979232"
---
# <span data-ttu-id="c158b-101">New-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="c158b-101">New-AzServiceFabricApplicationType</span></span>

## <span data-ttu-id="c158b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c158b-102">SYNOPSIS</span></span>
<span data-ttu-id="c158b-103">지정된 리소스 그룹 및 클러스터 아래에서 새 서비스 패브릭 애플리케이션 유형을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="c158b-103">Create new service fabric application type under the specified resource group and cluster.</span></span>

## <span data-ttu-id="c158b-104">구문</span><span class="sxs-lookup"><span data-stu-id="c158b-104">SYNTAX</span></span>

```
New-AzServiceFabricApplicationType [-ResourceGroupName] <String> [-ClusterName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c158b-105">설명</span><span class="sxs-lookup"><span data-stu-id="c158b-105">DESCRIPTION</span></span>
<span data-ttu-id="c158b-106">cmdlet은 지정된 리소스 그룹 및 클러스터 아래에 새 서비스 패브릭 애플리케이션 유형을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c158b-106">The cmdlet creates a new service fabric application type under the specified resource group and cluster.</span></span>

## <span data-ttu-id="c158b-107">예제</span><span class="sxs-lookup"><span data-stu-id="c158b-107">EXAMPLES</span></span>

### <span data-ttu-id="c158b-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="c158b-108">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appTypeName = "testAppType"
PS C:\> $appType = New-AzServiceFabricApplicationType -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appTypeName -Verbose
```

<span data-ttu-id="c158b-109">이 예제에서는 지정된 리소스 그룹 및 클러스터 아래에 새 애플리케이션 형식 "testAppType"을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="c158b-109">This example will create a new application type "testAppType" under the resource group and cluster specified.</span></span>

## <span data-ttu-id="c158b-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="c158b-110">PARAMETERS</span></span>

### <span data-ttu-id="c158b-111">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="c158b-111">-ClusterName</span></span>
<span data-ttu-id="c158b-112">클러스터의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c158b-112">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="c158b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c158b-113">-DefaultProfile</span></span>
<span data-ttu-id="c158b-114">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c158b-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c158b-115">-Name</span><span class="sxs-lookup"><span data-stu-id="c158b-115">-Name</span></span>
<span data-ttu-id="c158b-116">애플리케이션 형식의 이름 지정</span><span class="sxs-lookup"><span data-stu-id="c158b-116">Specify the name of the application type</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ApplicationTypeName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c158b-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c158b-117">-ResourceGroupName</span></span>
<span data-ttu-id="c158b-118">리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c158b-118">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="c158b-119">-확인</span><span class="sxs-lookup"><span data-stu-id="c158b-119">-Confirm</span></span>
<span data-ttu-id="c158b-120">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="c158b-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c158b-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c158b-121">-WhatIf</span></span>
<span data-ttu-id="c158b-122">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="c158b-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c158b-123">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c158b-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c158b-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c158b-124">CommonParameters</span></span>
<span data-ttu-id="c158b-125">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="c158b-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c158b-126">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c158b-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c158b-127">입력</span><span class="sxs-lookup"><span data-stu-id="c158b-127">INPUTS</span></span>

### <span data-ttu-id="c158b-128">System.String</span><span class="sxs-lookup"><span data-stu-id="c158b-128">System.String</span></span>

## <span data-ttu-id="c158b-129">출력</span><span class="sxs-lookup"><span data-stu-id="c158b-129">OUTPUTS</span></span>

### <span data-ttu-id="c158b-130">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplicationType</span><span class="sxs-lookup"><span data-stu-id="c158b-130">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplicationType</span></span>

## <span data-ttu-id="c158b-131">참고 사항</span><span class="sxs-lookup"><span data-stu-id="c158b-131">NOTES</span></span>

## <span data-ttu-id="c158b-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c158b-132">RELATED LINKS</span></span>
