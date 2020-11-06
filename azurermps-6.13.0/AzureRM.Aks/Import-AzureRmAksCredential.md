---
external help file: Microsoft.Azure.Commands.Aks.dll-Help.xml
Module Name: AzureRM.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.aks/import-azurermaks
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Aks/Commands.Aks/help/Import-AzureRmAksCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Aks/Commands.Aks/help/Import-AzureRmAksCredential.md
ms.openlocfilehash: b65ac736be5ee5f2f0592bcb2fdc84c873361f9f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93532548"
---
# <span data-ttu-id="5076b-101">Import-AzureRmAksCredential</span><span class="sxs-lookup"><span data-stu-id="5076b-101">Import-AzureRmAksCredential</span></span>

## <span data-ttu-id="5076b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5076b-102">SYNOPSIS</span></span>
<span data-ttu-id="5076b-103">관리 되는 Kubernetes 클러스터에 대 한 Kubectl config를 가져오고 병합 합니다.</span><span class="sxs-lookup"><span data-stu-id="5076b-103">Import and merge Kubectl config for a managed Kubernetes Cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5076b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="5076b-104">SYNTAX</span></span>

### <span data-ttu-id="5076b-105">GroupNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="5076b-105">GroupNameParameterSet (Default)</span></span>
```
Import-AzureRmAksCredential [-ResourceGroupName] <String> [-Name] <String> [-Admin] [-ConfigPath <String>]
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5076b-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5076b-106">InputObjectParameterSet</span></span>
```
Import-AzureRmAksCredential -InputObject <PSKubernetesCluster> [-Admin] [-ConfigPath <String>] [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5076b-107">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5076b-107">IdParameterSet</span></span>
```
Import-AzureRmAksCredential [-Id] <String> [-Admin] [-ConfigPath <String>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5076b-108">설명은</span><span class="sxs-lookup"><span data-stu-id="5076b-108">DESCRIPTION</span></span>
<span data-ttu-id="5076b-109">관리 되는 Kubernetes 클러스터에 대 한 Kubectl config를 가져오고 병합 합니다.</span><span class="sxs-lookup"><span data-stu-id="5076b-109">Import and merge Kubectl config for a managed Kubernetes Cluster.</span></span>

## <span data-ttu-id="5076b-110">예제의</span><span class="sxs-lookup"><span data-stu-id="5076b-110">EXAMPLES</span></span>

### <span data-ttu-id="5076b-111">Kubectl config 가져오기 및 병합</span><span class="sxs-lookup"><span data-stu-id="5076b-111">Import and merge Kubectl config</span></span>
```
PS C:\> Import-AzureRmAksCredential -ResourceGroupName group -Name myCluster
```

## <span data-ttu-id="5076b-112">변수</span><span class="sxs-lookup"><span data-stu-id="5076b-112">PARAMETERS</span></span>

### <span data-ttu-id="5076b-113">-관리자</span><span class="sxs-lookup"><span data-stu-id="5076b-113">-Admin</span></span>
<span data-ttu-id="5076b-114">기본 ' Clusteradmin' ' 대신 ' clusterAdmin' kubectl config를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="5076b-114">Get the 'clusterAdmin' kubectl config instead of the default 'clusterUser'.</span></span>

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

### <span data-ttu-id="5076b-115">-ConfigPath</span><span class="sxs-lookup"><span data-stu-id="5076b-115">-ConfigPath</span></span>
<span data-ttu-id="5076b-116">만들거나 업데이트할 kubectl config 파일입니다.</span><span class="sxs-lookup"><span data-stu-id="5076b-116">A kubectl config file to create or update.</span></span>
<span data-ttu-id="5076b-117">'-'을 사용 하 여 YAML를 대신 stdout에 인쇄 합니다.</span><span class="sxs-lookup"><span data-stu-id="5076b-117">Use '-' to print YAML to stdout instead.</span></span> <span data-ttu-id="5076b-118">기본값:% Home%/.kube/config.</span><span class="sxs-lookup"><span data-stu-id="5076b-118">Default: %Home%/.kube/config.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5076b-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5076b-119">-DefaultProfile</span></span>
<span data-ttu-id="5076b-120">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="5076b-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5076b-121">-Force</span><span class="sxs-lookup"><span data-stu-id="5076b-121">-Force</span></span>
<span data-ttu-id="5076b-122">Default 인 경우에도 Kubernetes config 가져오기</span><span class="sxs-lookup"><span data-stu-id="5076b-122">Import Kubernetes config even if it is the default</span></span>

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

### <span data-ttu-id="5076b-123">-Id</span><span class="sxs-lookup"><span data-stu-id="5076b-123">-Id</span></span>
<span data-ttu-id="5076b-124">관리 되는 Kubernetes 클러스터의 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="5076b-124">Id of a managed Kubernetes cluster</span></span>

```yaml
Type: System.String
Parameter Sets: IdParameterSet
Aliases: ResourceId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5076b-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5076b-125">-InputObject</span></span>
<span data-ttu-id="5076b-126">일반적으로 파이프라인을 통해 전달 되는 P고 U칭찬 Netescluster 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="5076b-126">A PSKubernetesCluster object, normally passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5076b-127">-이름</span><span class="sxs-lookup"><span data-stu-id="5076b-127">-Name</span></span>
<span data-ttu-id="5076b-128">관리 되는 Kubernetes 클러스터의 이름</span><span class="sxs-lookup"><span data-stu-id="5076b-128">Name of your managed Kubernetes cluster</span></span>

```yaml
Type: System.String
Parameter Sets: GroupNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5076b-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5076b-129">-PassThru</span></span>
<span data-ttu-id="5076b-130">가져오기가 성공한 경우 true를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="5076b-130">Returns true if import is successful</span></span>

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

### <span data-ttu-id="5076b-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5076b-131">-ResourceGroupName</span></span>
<span data-ttu-id="5076b-132">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="5076b-132">Resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: GroupNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5076b-133">-확인</span><span class="sxs-lookup"><span data-stu-id="5076b-133">-Confirm</span></span>
<span data-ttu-id="5076b-134">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="5076b-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5076b-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5076b-135">-WhatIf</span></span>
<span data-ttu-id="5076b-136">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="5076b-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5076b-137">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5076b-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5076b-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5076b-138">CommonParameters</span></span>
<span data-ttu-id="5076b-139">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="5076b-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5076b-140">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5076b-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5076b-141">입력</span><span class="sxs-lookup"><span data-stu-id="5076b-141">INPUTS</span></span>

### <span data-ttu-id="5076b-142">Aks. p U Netescluster</span><span class="sxs-lookup"><span data-stu-id="5076b-142">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>
<span data-ttu-id="5076b-143">매개 변수: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="5076b-143">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="5076b-144">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="5076b-144">System.String</span></span>

## <span data-ttu-id="5076b-145">출력</span><span class="sxs-lookup"><span data-stu-id="5076b-145">OUTPUTS</span></span>

### <span data-ttu-id="5076b-146">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="5076b-146">System.String</span></span>

## <span data-ttu-id="5076b-147">상속자</span><span class="sxs-lookup"><span data-stu-id="5076b-147">NOTES</span></span>

## <span data-ttu-id="5076b-148">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5076b-148">RELATED LINKS</span></span>
