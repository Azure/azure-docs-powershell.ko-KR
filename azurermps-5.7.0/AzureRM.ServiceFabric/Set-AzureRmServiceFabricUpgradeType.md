---
external help file: Microsoft.Azure.Commands.ServiceFabric.dll-Help.xml
Module Name: AzureRM.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicefabric/set-azurermservicefabricupgradetype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Set-AzureRmServiceFabricUpgradeType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Set-AzureRmServiceFabricUpgradeType.md
ms.openlocfilehash: 8a675355806a8b4579abcea965a5e0e0b8128207
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93534647"
---
# <span data-ttu-id="e32da-101">Set-AzureRmServiceFabricUpgradeType</span><span class="sxs-lookup"><span data-stu-id="e32da-101">Set-AzureRmServiceFabricUpgradeType</span></span>

## <span data-ttu-id="e32da-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e32da-102">SYNOPSIS</span></span>
<span data-ttu-id="e32da-103">클러스터의 Service Fabric 업그레이드 유형을 변경 합니다.</span><span class="sxs-lookup"><span data-stu-id="e32da-103">Change the Service Fabric upgrade type of the cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e32da-104">구문과</span><span class="sxs-lookup"><span data-stu-id="e32da-104">SYNTAX</span></span>

### <span data-ttu-id="e32da-105">자동 번역</span><span class="sxs-lookup"><span data-stu-id="e32da-105">Automatic</span></span>
```
Set-AzureRmServiceFabricUpgradeType [-ResourceGroupName] <String> [-Name] <String>
 -UpgradeMode <ClusterUpgradeMode> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e32da-106">수동</span><span class="sxs-lookup"><span data-stu-id="e32da-106">Manual</span></span>
```
Set-AzureRmServiceFabricUpgradeType [-ResourceGroupName] <String> [-Name] <String>
 -UpgradeMode <ClusterUpgradeMode> -Version <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e32da-107">설명은</span><span class="sxs-lookup"><span data-stu-id="e32da-107">DESCRIPTION</span></span>
<span data-ttu-id="e32da-108">**Set-AzureRmServiceFabricUpgradeType** 를 사용 하 여 특정 서비스 패브릭 코드 버전을 사용 하 여 업그레이드 유형을 자동 또는 수동으로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e32da-108">Use **Set-AzureRmServiceFabricUpgradeType** to set upgrade type to automatic or manual with specific Service Fabric code version.</span></span>

## <span data-ttu-id="e32da-109">예제의</span><span class="sxs-lookup"><span data-stu-id="e32da-109">EXAMPLES</span></span>

### <span data-ttu-id="e32da-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="e32da-110">Example 1</span></span>
```
PS c:> Set-AzureRmServiceFabricUpgradeType -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster'  -UpgradeMode Automatic
```

<span data-ttu-id="e32da-111">이 명령을 실행할 때 클러스터 업그레이드 모드가 자동으로 설정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="e32da-111">This command will set the cluster upgrade mode to automatic.</span></span>

## <span data-ttu-id="e32da-112">변수</span><span class="sxs-lookup"><span data-stu-id="e32da-112">PARAMETERS</span></span>

### <span data-ttu-id="e32da-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e32da-113">-DefaultProfile</span></span>
<span data-ttu-id="e32da-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e32da-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e32da-115">-이름</span><span class="sxs-lookup"><span data-stu-id="e32da-115">-Name</span></span>
<span data-ttu-id="e32da-116">클러스터의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e32da-116">Specify the name of the cluster.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ClusterName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e32da-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e32da-117">-ResourceGroupName</span></span>
<span data-ttu-id="e32da-118">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e32da-118">Specifies the name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e32da-119">-UpgradeMode</span><span class="sxs-lookup"><span data-stu-id="e32da-119">-UpgradeMode</span></span>
<span data-ttu-id="e32da-120">ClusterUpgradeMode</span><span class="sxs-lookup"><span data-stu-id="e32da-120">ClusterUpgradeMode</span></span>

```yaml
Type: ClusterUpgradeMode
Parameter Sets: (All)
Aliases: 
Accepted values: Automatic, Manual

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e32da-121">-버전</span><span class="sxs-lookup"><span data-stu-id="e32da-121">-Version</span></span>
<span data-ttu-id="e32da-122">클러스터 코드 버전.</span><span class="sxs-lookup"><span data-stu-id="e32da-122">Cluster code version.</span></span>

```yaml
Type: String
Parameter Sets: Manual
Aliases: ClusterCodeVersion

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e32da-123">-확인</span><span class="sxs-lookup"><span data-stu-id="e32da-123">-Confirm</span></span>
<span data-ttu-id="e32da-124">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="e32da-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e32da-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e32da-125">-WhatIf</span></span>
<span data-ttu-id="e32da-126">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="e32da-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e32da-127">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e32da-127">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e32da-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e32da-128">CommonParameters</span></span>
<span data-ttu-id="e32da-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e32da-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e32da-130">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e32da-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e32da-131">입력</span><span class="sxs-lookup"><span data-stu-id="e32da-131">INPUTS</span></span>

### <span data-ttu-id="e32da-132">ServiceFabric. a m/. ClusterUpgradeMode</span><span class="sxs-lookup"><span data-stu-id="e32da-132">Microsoft.Azure.Commands.ServiceFabric.Models.ClusterUpgradeMode</span></span>
<span data-ttu-id="e32da-133">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="e32da-133">System.String</span></span>

## <span data-ttu-id="e32da-134">출력</span><span class="sxs-lookup"><span data-stu-id="e32da-134">OUTPUTS</span></span>

### <span data-ttu-id="e32da-135">ServiceFabric 클러스터의 모든.</span><span class="sxs-lookup"><span data-stu-id="e32da-135">Microsoft.Azure.Commands.ServiceFabric.Models.PsCluster</span></span>

## <span data-ttu-id="e32da-136">상속자</span><span class="sxs-lookup"><span data-stu-id="e32da-136">NOTES</span></span>

## <span data-ttu-id="e32da-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e32da-137">RELATED LINKS</span></span>

