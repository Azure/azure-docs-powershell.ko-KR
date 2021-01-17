---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/set-azservicefabricupgradetype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Set-AzServiceFabricUpgradeType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Set-AzServiceFabricUpgradeType.md
ms.openlocfilehash: 346bb9cb073488d0112ea08db22fb1f6c387bac9
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98345458"
---
# <span data-ttu-id="a73cb-101">Set-AzServiceFabricUpgradeType</span><span class="sxs-lookup"><span data-stu-id="a73cb-101">Set-AzServiceFabricUpgradeType</span></span>

## <span data-ttu-id="a73cb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a73cb-102">SYNOPSIS</span></span>
<span data-ttu-id="a73cb-103">클러스터의 Service Fabric 업그레이드 유형을 변경합니다.</span><span class="sxs-lookup"><span data-stu-id="a73cb-103">Change the Service Fabric upgrade type of the cluster.</span></span>

## <span data-ttu-id="a73cb-104">구문</span><span class="sxs-lookup"><span data-stu-id="a73cb-104">SYNTAX</span></span>

### <span data-ttu-id="a73cb-105">자동 번역</span><span class="sxs-lookup"><span data-stu-id="a73cb-105">Automatic</span></span>
```
Set-AzServiceFabricUpgradeType [-ResourceGroupName] <String> [-Name] <String> -UpgradeMode <ClusterUpgradeMode>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a73cb-106">수동</span><span class="sxs-lookup"><span data-stu-id="a73cb-106">Manual</span></span>
```
Set-AzServiceFabricUpgradeType [-ResourceGroupName] <String> [-Name] <String> -UpgradeMode <ClusterUpgradeMode>
 -Version <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a73cb-107">설명</span><span class="sxs-lookup"><span data-stu-id="a73cb-107">DESCRIPTION</span></span>
<span data-ttu-id="a73cb-108">**Set-AzServiceFabricUpgradeType을** 사용하여 특정 Service Fabric 코드 버전에서 자동 또는 수동으로 업그레이드 유형을 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a73cb-108">Use **Set-AzServiceFabricUpgradeType** to set upgrade type to automatic or manual with specific Service Fabric code version.</span></span>

## <span data-ttu-id="a73cb-109">예제</span><span class="sxs-lookup"><span data-stu-id="a73cb-109">EXAMPLES</span></span>

### <span data-ttu-id="a73cb-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="a73cb-110">Example 1</span></span>
```
PS c:> Set-AzServiceFabricUpgradeType -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster'  -UpgradeMode Automatic
```

<span data-ttu-id="a73cb-111">이 명령은 클러스터 업그레이드 모드를 자동으로 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="a73cb-111">This command will set the cluster upgrade mode to automatic.</span></span>

## <span data-ttu-id="a73cb-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a73cb-112">PARAMETERS</span></span>

### <span data-ttu-id="a73cb-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a73cb-113">-DefaultProfile</span></span>
<span data-ttu-id="a73cb-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a73cb-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a73cb-115">-Name</span><span class="sxs-lookup"><span data-stu-id="a73cb-115">-Name</span></span>
<span data-ttu-id="a73cb-116">클러스터의 이름 지정</span><span class="sxs-lookup"><span data-stu-id="a73cb-116">Specify the name of the cluster</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ClusterName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a73cb-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a73cb-117">-ResourceGroupName</span></span>
<span data-ttu-id="a73cb-118">리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a73cb-118">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="a73cb-119">-UpgradeMode</span><span class="sxs-lookup"><span data-stu-id="a73cb-119">-UpgradeMode</span></span>
<span data-ttu-id="a73cb-120">ClusterUpgradeMode</span><span class="sxs-lookup"><span data-stu-id="a73cb-120">ClusterUpgradeMode</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceFabric.Models.ClusterUpgradeMode
Parameter Sets: (All)
Aliases:
Accepted values: Automatic, Manual

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a73cb-121">-Version</span><span class="sxs-lookup"><span data-stu-id="a73cb-121">-Version</span></span>
<span data-ttu-id="a73cb-122">클러스터 코드 버전</span><span class="sxs-lookup"><span data-stu-id="a73cb-122">Cluster code version</span></span>

```yaml
Type: System.String
Parameter Sets: Manual
Aliases: ClusterCodeVersion

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a73cb-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a73cb-123">-Confirm</span></span>
<span data-ttu-id="a73cb-124">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="a73cb-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a73cb-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a73cb-125">-WhatIf</span></span>
<span data-ttu-id="a73cb-126">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="a73cb-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a73cb-127">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a73cb-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a73cb-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a73cb-128">CommonParameters</span></span>
<span data-ttu-id="a73cb-129">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="a73cb-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a73cb-130">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="a73cb-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a73cb-131">입력</span><span class="sxs-lookup"><span data-stu-id="a73cb-131">INPUTS</span></span>

### <span data-ttu-id="a73cb-132">System.String</span><span class="sxs-lookup"><span data-stu-id="a73cb-132">System.String</span></span>

### <span data-ttu-id="a73cb-133">Microsoft.Azure.Commands.ServiceFabric.Models.ClusterUpgradeMode</span><span class="sxs-lookup"><span data-stu-id="a73cb-133">Microsoft.Azure.Commands.ServiceFabric.Models.ClusterUpgradeMode</span></span>

## <span data-ttu-id="a73cb-134">출력</span><span class="sxs-lookup"><span data-stu-id="a73cb-134">OUTPUTS</span></span>

### <span data-ttu-id="a73cb-135">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span><span class="sxs-lookup"><span data-stu-id="a73cb-135">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="a73cb-136">참고 사항</span><span class="sxs-lookup"><span data-stu-id="a73cb-136">NOTES</span></span>

## <span data-ttu-id="a73cb-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a73cb-137">RELATED LINKS</span></span>
