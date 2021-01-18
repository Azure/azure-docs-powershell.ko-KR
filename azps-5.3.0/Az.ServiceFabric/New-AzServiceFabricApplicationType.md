---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/new-azservicefabricapplicationtype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/New-AzServiceFabricApplicationType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/New-AzServiceFabricApplicationType.md
ms.openlocfilehash: 690b00c41aea571786916d2055eb4063c51c4370
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98494775"
---
# <span data-ttu-id="31692-101">New-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="31692-101">New-AzServiceFabricApplicationType</span></span>

## <span data-ttu-id="31692-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="31692-102">SYNOPSIS</span></span>
<span data-ttu-id="31692-103">지정된 리소스 그룹 및 클러스터 아래에 새 Service Fabric 애플리케이션 유형을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="31692-103">Create new service fabric application type under the specified resource group and cluster.</span></span>

## <span data-ttu-id="31692-104">구문</span><span class="sxs-lookup"><span data-stu-id="31692-104">SYNTAX</span></span>

```
New-AzServiceFabricApplicationType [-ResourceGroupName] <String> [-ClusterName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="31692-105">설명</span><span class="sxs-lookup"><span data-stu-id="31692-105">DESCRIPTION</span></span>
<span data-ttu-id="31692-106">이 cmdlet은 지정된 리소스 그룹 및 클러스터 아래에 새 Service Fabric 애플리케이션 유형을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="31692-106">The cmdlet creates a new service fabric application type under the specified resource group and cluster.</span></span>

## <span data-ttu-id="31692-107">예제</span><span class="sxs-lookup"><span data-stu-id="31692-107">EXAMPLES</span></span>

### <span data-ttu-id="31692-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="31692-108">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appTypeName = "testAppType"
PS C:\> $appType = New-AzServiceFabricApplicationType -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appTypeName -Verbose
```

<span data-ttu-id="31692-109">이 예제에서는 지정된 리소스 그룹 및 클러스터 아래에 새 애플리케이션 유형 "testAppType"을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="31692-109">This example will create a new application type "testAppType" under the resource group and cluster specified.</span></span>

## <span data-ttu-id="31692-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="31692-110">PARAMETERS</span></span>

### <span data-ttu-id="31692-111">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="31692-111">-ClusterName</span></span>
<span data-ttu-id="31692-112">클러스터의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="31692-112">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="31692-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="31692-113">-DefaultProfile</span></span>
<span data-ttu-id="31692-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="31692-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="31692-115">-Name</span><span class="sxs-lookup"><span data-stu-id="31692-115">-Name</span></span>
<span data-ttu-id="31692-116">애플리케이션 형식의 이름 지정</span><span class="sxs-lookup"><span data-stu-id="31692-116">Specify the name of the application type</span></span>

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

### <span data-ttu-id="31692-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="31692-117">-ResourceGroupName</span></span>
<span data-ttu-id="31692-118">리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="31692-118">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="31692-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="31692-119">-Confirm</span></span>
<span data-ttu-id="31692-120">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="31692-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="31692-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="31692-121">-WhatIf</span></span>
<span data-ttu-id="31692-122">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="31692-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="31692-123">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="31692-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="31692-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31692-124">CommonParameters</span></span>
<span data-ttu-id="31692-125">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="31692-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31692-126">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="31692-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31692-127">입력</span><span class="sxs-lookup"><span data-stu-id="31692-127">INPUTS</span></span>

### <span data-ttu-id="31692-128">System.String</span><span class="sxs-lookup"><span data-stu-id="31692-128">System.String</span></span>

## <span data-ttu-id="31692-129">출력</span><span class="sxs-lookup"><span data-stu-id="31692-129">OUTPUTS</span></span>

### <span data-ttu-id="31692-130">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplicationType</span><span class="sxs-lookup"><span data-stu-id="31692-130">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplicationType</span></span>

## <span data-ttu-id="31692-131">참고 사항</span><span class="sxs-lookup"><span data-stu-id="31692-131">NOTES</span></span>

## <span data-ttu-id="31692-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="31692-132">RELATED LINKS</span></span>
