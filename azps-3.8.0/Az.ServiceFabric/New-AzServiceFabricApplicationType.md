---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/new-azservicefabricapplicationtype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/New-AzServiceFabricApplicationType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/New-AzServiceFabricApplicationType.md
ms.openlocfilehash: 2e878c562c8f60ecebc9b6a43b3980e06fd0e355
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94041722"
---
# <span data-ttu-id="ce752-101">New-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="ce752-101">New-AzServiceFabricApplicationType</span></span>

## <span data-ttu-id="ce752-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ce752-102">SYNOPSIS</span></span>
<span data-ttu-id="ce752-103">지정 된 리소스 그룹 및 클러스터 아래에 새 service fabric 응용 프로그램 종류를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ce752-103">Create new service fabric application type under the specified resource group and cluster.</span></span>

## <span data-ttu-id="ce752-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ce752-104">SYNTAX</span></span>

```
New-AzServiceFabricApplicationType [-ResourceGroupName] <String> [-ClusterName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ce752-105">설명은</span><span class="sxs-lookup"><span data-stu-id="ce752-105">DESCRIPTION</span></span>
<span data-ttu-id="ce752-106">Cmdlet은 지정 된 리소스 그룹 및 클러스터 아래에 새 서비스 패브릭 응용 프로그램 종류를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ce752-106">The cmdlet creates a new service fabric application type under the specified resource group and cluster.</span></span>

## <span data-ttu-id="ce752-107">예제의</span><span class="sxs-lookup"><span data-stu-id="ce752-107">EXAMPLES</span></span>

### <span data-ttu-id="ce752-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="ce752-108">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appTypeName = "testAppType"
PS C:\> $appType = New-AzServiceFabricApplicationType -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appTypeName -Verbose
```

<span data-ttu-id="ce752-109">이 예제에서는 리소스 그룹 및 클러스터에 지정 된 새 응용 프로그램 유형 "testAppType"를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ce752-109">This example will create a new application type "testAppType" under the resource group and cluster specified.</span></span>

## <span data-ttu-id="ce752-110">변수</span><span class="sxs-lookup"><span data-stu-id="ce752-110">PARAMETERS</span></span>

### <span data-ttu-id="ce752-111">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="ce752-111">-ClusterName</span></span>
<span data-ttu-id="ce752-112">클러스터의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ce752-112">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="ce752-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ce752-113">-DefaultProfile</span></span>
<span data-ttu-id="ce752-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ce752-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ce752-115">-이름</span><span class="sxs-lookup"><span data-stu-id="ce752-115">-Name</span></span>
<span data-ttu-id="ce752-116">응용 프로그램 종류의 이름 지정</span><span class="sxs-lookup"><span data-stu-id="ce752-116">Specify the name of the application type</span></span>

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

### <span data-ttu-id="ce752-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ce752-117">-ResourceGroupName</span></span>
<span data-ttu-id="ce752-118">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ce752-118">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="ce752-119">-확인</span><span class="sxs-lookup"><span data-stu-id="ce752-119">-Confirm</span></span>
<span data-ttu-id="ce752-120">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="ce752-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ce752-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ce752-121">-WhatIf</span></span>
<span data-ttu-id="ce752-122">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="ce752-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ce752-123">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ce752-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ce752-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce752-124">CommonParameters</span></span>
<span data-ttu-id="ce752-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ce752-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ce752-126">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ce752-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ce752-127">입력</span><span class="sxs-lookup"><span data-stu-id="ce752-127">INPUTS</span></span>

### <span data-ttu-id="ce752-128">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="ce752-128">System.String</span></span>

## <span data-ttu-id="ce752-129">출력</span><span class="sxs-lookup"><span data-stu-id="ce752-129">OUTPUTS</span></span>

### <span data-ttu-id="ce752-130">ServiceFabric. m a m/. m i m m Applicationtype</span><span class="sxs-lookup"><span data-stu-id="ce752-130">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplicationType</span></span>

## <span data-ttu-id="ce752-131">상속자</span><span class="sxs-lookup"><span data-stu-id="ce752-131">NOTES</span></span>

## <span data-ttu-id="ce752-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ce752-132">RELATED LINKS</span></span>
