---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/set-azservicefabricupgradetype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Set-AzServiceFabricUpgradeType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Set-AzServiceFabricUpgradeType.md
ms.openlocfilehash: c29a1bf4b5b60034a8f38ff8388f36997dbddfc7
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94044293"
---
# <span data-ttu-id="01876-101">Set-AzServiceFabricUpgradeType</span><span class="sxs-lookup"><span data-stu-id="01876-101">Set-AzServiceFabricUpgradeType</span></span>

## <span data-ttu-id="01876-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="01876-102">SYNOPSIS</span></span>
<span data-ttu-id="01876-103">클러스터의 Service Fabric 업그레이드 유형을 변경 합니다.</span><span class="sxs-lookup"><span data-stu-id="01876-103">Change the Service Fabric upgrade type of the cluster.</span></span>

## <span data-ttu-id="01876-104">구문과</span><span class="sxs-lookup"><span data-stu-id="01876-104">SYNTAX</span></span>

### <span data-ttu-id="01876-105">자동 번역</span><span class="sxs-lookup"><span data-stu-id="01876-105">Automatic</span></span>
```
Set-AzServiceFabricUpgradeType [-ResourceGroupName] <String> [-Name] <String> -UpgradeMode <ClusterUpgradeMode>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="01876-106">수동</span><span class="sxs-lookup"><span data-stu-id="01876-106">Manual</span></span>
```
Set-AzServiceFabricUpgradeType [-ResourceGroupName] <String> [-Name] <String> -UpgradeMode <ClusterUpgradeMode>
 -Version <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="01876-107">설명은</span><span class="sxs-lookup"><span data-stu-id="01876-107">DESCRIPTION</span></span>
<span data-ttu-id="01876-108">**Set-AzServiceFabricUpgradeType** 를 사용 하 여 특정 서비스 패브릭 코드 버전을 사용 하 여 업그레이드 유형을 자동 또는 수동으로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="01876-108">Use **Set-AzServiceFabricUpgradeType** to set upgrade type to automatic or manual with specific Service Fabric code version.</span></span>

## <span data-ttu-id="01876-109">예제의</span><span class="sxs-lookup"><span data-stu-id="01876-109">EXAMPLES</span></span>

### <span data-ttu-id="01876-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="01876-110">Example 1</span></span>
```
PS c:> Set-AzServiceFabricUpgradeType -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster'  -UpgradeMode Automatic
```

<span data-ttu-id="01876-111">이 명령을 실행할 때 클러스터 업그레이드 모드가 자동으로 설정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="01876-111">This command will set the cluster upgrade mode to automatic.</span></span>

## <span data-ttu-id="01876-112">변수</span><span class="sxs-lookup"><span data-stu-id="01876-112">PARAMETERS</span></span>

### <span data-ttu-id="01876-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="01876-113">-DefaultProfile</span></span>
<span data-ttu-id="01876-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="01876-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="01876-115">-이름</span><span class="sxs-lookup"><span data-stu-id="01876-115">-Name</span></span>
<span data-ttu-id="01876-116">클러스터 이름 지정</span><span class="sxs-lookup"><span data-stu-id="01876-116">Specify the name of the cluster</span></span>

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

### <span data-ttu-id="01876-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="01876-117">-ResourceGroupName</span></span>
<span data-ttu-id="01876-118">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="01876-118">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="01876-119">-UpgradeMode</span><span class="sxs-lookup"><span data-stu-id="01876-119">-UpgradeMode</span></span>
<span data-ttu-id="01876-120">ClusterUpgradeMode</span><span class="sxs-lookup"><span data-stu-id="01876-120">ClusterUpgradeMode</span></span>

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

### <span data-ttu-id="01876-121">-버전</span><span class="sxs-lookup"><span data-stu-id="01876-121">-Version</span></span>
<span data-ttu-id="01876-122">클러스터 코드 버전</span><span class="sxs-lookup"><span data-stu-id="01876-122">Cluster code version</span></span>

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

### <span data-ttu-id="01876-123">-확인</span><span class="sxs-lookup"><span data-stu-id="01876-123">-Confirm</span></span>
<span data-ttu-id="01876-124">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="01876-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="01876-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="01876-125">-WhatIf</span></span>
<span data-ttu-id="01876-126">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="01876-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="01876-127">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="01876-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="01876-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01876-128">CommonParameters</span></span>
<span data-ttu-id="01876-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="01876-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01876-130">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="01876-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01876-131">입력</span><span class="sxs-lookup"><span data-stu-id="01876-131">INPUTS</span></span>

### <span data-ttu-id="01876-132">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="01876-132">System.String</span></span>

### <span data-ttu-id="01876-133">ServiceFabric. a m/. ClusterUpgradeMode</span><span class="sxs-lookup"><span data-stu-id="01876-133">Microsoft.Azure.Commands.ServiceFabric.Models.ClusterUpgradeMode</span></span>

## <span data-ttu-id="01876-134">출력</span><span class="sxs-lookup"><span data-stu-id="01876-134">OUTPUTS</span></span>

### <span data-ttu-id="01876-135">ServiceFabric 클러스터의 모든.</span><span class="sxs-lookup"><span data-stu-id="01876-135">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="01876-136">상속자</span><span class="sxs-lookup"><span data-stu-id="01876-136">NOTES</span></span>

## <span data-ttu-id="01876-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="01876-137">RELATED LINKS</span></span>
