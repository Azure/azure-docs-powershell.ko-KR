---
external help file: Microsoft.Azure.Commands.Aks.dll-Help.xml
Module Name: AzureRM.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.aks/remove-azurermaks
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Aks/Commands.Aks/help/Remove-AzureRmAks.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Aks/Commands.Aks/help/Remove-AzureRmAks.md
ms.openlocfilehash: 1843322f702f8c43f97f1cf64c9d9f5b92d419bd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93532888"
---
# <span data-ttu-id="1a9bf-101">Remove-AzureRmAks</span><span class="sxs-lookup"><span data-stu-id="1a9bf-101">Remove-AzureRmAks</span></span>

## <span data-ttu-id="1a9bf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1a9bf-102">SYNOPSIS</span></span>
<span data-ttu-id="1a9bf-103">관리 Kubernetes 클러스터를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="1a9bf-103">Delete a managed Kubernetes cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1a9bf-104">구문과</span><span class="sxs-lookup"><span data-stu-id="1a9bf-104">SYNTAX</span></span>

### <span data-ttu-id="1a9bf-105">GroupNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="1a9bf-105">GroupNameParameterSet (Default)</span></span>
```
Remove-AzureRmAks [-ResourceGroupName] <String> [-Name] <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1a9bf-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1a9bf-106">InputObjectParameterSet</span></span>
```
Remove-AzureRmAks -InputObject <PSKubernetesCluster> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1a9bf-107">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1a9bf-107">IdParameterSet</span></span>
```
Remove-AzureRmAks [-Id] <String> [-PassThru] [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1a9bf-108">설명은</span><span class="sxs-lookup"><span data-stu-id="1a9bf-108">DESCRIPTION</span></span>
<span data-ttu-id="1a9bf-109">관리 Kubernetes 클러스터를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="1a9bf-109">Delete a managed Kubernetes cluster.</span></span>

## <span data-ttu-id="1a9bf-110">예제의</span><span class="sxs-lookup"><span data-stu-id="1a9bf-110">EXAMPLES</span></span>

### <span data-ttu-id="1a9bf-111">기존 관리 Kubernetes 클러스터 삭제</span><span class="sxs-lookup"><span data-stu-id="1a9bf-111">Delete an existing managed Kubernetes cluster</span></span>
```
PS C:\> Remove-AzureRmAks -ResourceGroupName group -Name myCluster
```

## <span data-ttu-id="1a9bf-112">변수</span><span class="sxs-lookup"><span data-stu-id="1a9bf-112">PARAMETERS</span></span>

### <span data-ttu-id="1a9bf-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1a9bf-113">-AsJob</span></span>
<span data-ttu-id="1a9bf-114">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="1a9bf-114">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1a9bf-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1a9bf-115">-DefaultProfile</span></span>
<span data-ttu-id="1a9bf-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="1a9bf-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1a9bf-117">-Force</span><span class="sxs-lookup"><span data-stu-id="1a9bf-117">-Force</span></span>
<span data-ttu-id="1a9bf-118">메시지를 표시 하지 않고 관리 Kubernetes 클러스터 제거</span><span class="sxs-lookup"><span data-stu-id="1a9bf-118">Remove managed Kubernetes cluster without prompt</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1a9bf-119">-Id</span><span class="sxs-lookup"><span data-stu-id="1a9bf-119">-Id</span></span>
<span data-ttu-id="1a9bf-120">관리 되는 Kubernetes 클러스터의 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="1a9bf-120">Id of a managed Kubernetes cluster</span></span>

```yaml
Type: String
Parameter Sets: IdParameterSet
Aliases: ResourceId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1a9bf-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1a9bf-121">-InputObject</span></span>
<span data-ttu-id="1a9bf-122">일반적으로 파이프라인을 통해 전달 되는 P고 U칭찬 Netescluster 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="1a9bf-122">A PSKubernetesCluster object, normally passed through the pipeline.</span></span>

```yaml
Type: PSKubernetesCluster
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1a9bf-123">-이름</span><span class="sxs-lookup"><span data-stu-id="1a9bf-123">-Name</span></span>
<span data-ttu-id="1a9bf-124">관리 되는 Kubernetes 클러스터의 이름</span><span class="sxs-lookup"><span data-stu-id="1a9bf-124">Name of your managed Kubernetes cluster</span></span>

```yaml
Type: String
Parameter Sets: GroupNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1a9bf-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1a9bf-125">-PassThru</span></span>
<span data-ttu-id="1a9bf-126">삭제에 성공한 경우 true를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="1a9bf-126">Returns true if deletion is successful</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1a9bf-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1a9bf-127">-ResourceGroupName</span></span>
<span data-ttu-id="1a9bf-128">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="1a9bf-128">Resource group name</span></span>

```yaml
Type: String
Parameter Sets: GroupNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1a9bf-129">-확인</span><span class="sxs-lookup"><span data-stu-id="1a9bf-129">-Confirm</span></span>
<span data-ttu-id="1a9bf-130">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="1a9bf-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1a9bf-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1a9bf-131">-WhatIf</span></span>
<span data-ttu-id="1a9bf-132">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="1a9bf-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1a9bf-133">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1a9bf-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1a9bf-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a9bf-134">CommonParameters</span></span>
<span data-ttu-id="1a9bf-135">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="1a9bf-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a9bf-136">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1a9bf-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a9bf-137">입력</span><span class="sxs-lookup"><span data-stu-id="1a9bf-137">INPUTS</span></span>

### <span data-ttu-id="1a9bf-138">Aks. p U<c13> Netescluster</span><span class="sxs-lookup"><span data-stu-id="1a9bf-138">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>
<span data-ttu-id="1a9bf-139">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="1a9bf-139">System.String</span></span>

## <span data-ttu-id="1a9bf-140">출력</span><span class="sxs-lookup"><span data-stu-id="1a9bf-140">OUTPUTS</span></span>

### <span data-ttu-id="1a9bf-141">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="1a9bf-141">System.Boolean</span></span>

## <span data-ttu-id="1a9bf-142">상속자</span><span class="sxs-lookup"><span data-stu-id="1a9bf-142">NOTES</span></span>

## <span data-ttu-id="1a9bf-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1a9bf-143">RELATED LINKS</span></span>
