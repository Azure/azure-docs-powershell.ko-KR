---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: C3DD193E-B8FE-468D-BEE7-00C3D99B469E
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azresourcegroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzResourceGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzResourceGroupDeployment.md
ms.openlocfilehash: f1bb3530c31305e5f70c80d7b520286da9878480
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94226547"
---
# <span data-ttu-id="932a8-101">Remove-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="932a8-101">Remove-AzResourceGroupDeployment</span></span>

## <span data-ttu-id="932a8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="932a8-102">SYNOPSIS</span></span>
<span data-ttu-id="932a8-103">리소스 그룹 배포 및 연결 된 작업을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="932a8-103">Removes a resource group deployment and any associated operations.</span></span>

## <span data-ttu-id="932a8-104">구문과</span><span class="sxs-lookup"><span data-stu-id="932a8-104">SYNTAX</span></span>

### <span data-ttu-id="932a8-105">RemoveByResourceGroupName (기본값)</span><span class="sxs-lookup"><span data-stu-id="932a8-105">RemoveByResourceGroupName (Default)</span></span>
```
Remove-AzResourceGroupDeployment [-ResourceGroupName] <String> [-Name] <String> [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="932a8-106">RemoveByResourceGroupDeploymentId</span><span class="sxs-lookup"><span data-stu-id="932a8-106">RemoveByResourceGroupDeploymentId</span></span>
```
Remove-AzResourceGroupDeployment -Id <String> [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="932a8-107">설명은</span><span class="sxs-lookup"><span data-stu-id="932a8-107">DESCRIPTION</span></span>

<span data-ttu-id="932a8-108">**AzResourceGroupDeployment** Cmdlet은 Azure 리소스 그룹 배포 및 연결 된 작업을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="932a8-108">The **Remove-AzResourceGroupDeployment** cmdlet removes an Azure resource group deployment and any associated operations.</span></span>

## <span data-ttu-id="932a8-109">예제의</span><span class="sxs-lookup"><span data-stu-id="932a8-109">EXAMPLES</span></span>

### <span data-ttu-id="932a8-110">예제 1: ResourceId를 사용 하 여 리소스 그룹 배포 제거</span><span class="sxs-lookup"><span data-stu-id="932a8-110">Example 1: Removes a resource group deployment with ResourceId</span></span>

```powershell
PS C:\>Remove-AzResourceGroupDeployment -ResourceId /subscriptions/{subId}/resourceGroups/testGroup/providers/Microsoft.Resources/deployments/testDeployment1

True
```

<span data-ttu-id="932a8-111">이 명령은 배포의 정규화 된 리소스 Id를 사용 하 여 리소스 그룹 배포를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="932a8-111">This command removes a resource group deployment with the fully qualified resource Id of the deployment.</span></span>
<span data-ttu-id="932a8-112">성공적으로 제거 되 면 true를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="932a8-112">Successful removal returns true.</span></span>

### <span data-ttu-id="932a8-113">예제 2: ResourceGroupName 및 Context.resourcename을 사용 하 여 리소스 그룹 배포 제거</span><span class="sxs-lookup"><span data-stu-id="932a8-113">Example 2: Removes a resource group deployment with ResourceGroupName and ResourceName</span></span>

```powershell
PS C:\>Remove-AzResourceGroupDeployment -ResourceGroupName testGroup -Name testDeployment1

True
```

<span data-ttu-id="932a8-114">이 명령은 제공 된 ResourceGroupName 및 Context.resourcename을 사용 하 여 리소스 그룹 배포를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="932a8-114">This command removes a resource group deployment with the provided ResourceGroupName and ResourceName.</span></span>
<span data-ttu-id="932a8-115">성공적으로 제거 되 면 true를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="932a8-115">Successful removal returns true.</span></span>

## <span data-ttu-id="932a8-116">변수</span><span class="sxs-lookup"><span data-stu-id="932a8-116">PARAMETERS</span></span>

### <span data-ttu-id="932a8-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="932a8-117">-DefaultProfile</span></span>
<span data-ttu-id="932a8-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="932a8-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="932a8-119">-Id</span><span class="sxs-lookup"><span data-stu-id="932a8-119">-Id</span></span>
<span data-ttu-id="932a8-120">제거할 리소스 그룹 배포의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="932a8-120">Specifies the ID of the resource group deployment to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByResourceGroupDeploymentId
Aliases: DeploymentId, ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="932a8-121">-이름</span><span class="sxs-lookup"><span data-stu-id="932a8-121">-Name</span></span>
<span data-ttu-id="932a8-122">제거할 리소스 그룹 배포의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="932a8-122">Specifies the name of the resource group deployment to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByResourceGroupName
Aliases: DeploymentName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="932a8-123">-Pre</span><span class="sxs-lookup"><span data-stu-id="932a8-123">-Pre</span></span>
<span data-ttu-id="932a8-124">이 cmdlet이 사용할 버전을 자동으로 결정 하는 경우 시험판 API 버전을 고려 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="932a8-124">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="932a8-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="932a8-125">-ResourceGroupName</span></span>
<span data-ttu-id="932a8-126">제거할 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="932a8-126">Specifies the name of the resource group to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByResourceGroupName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="932a8-127">-확인</span><span class="sxs-lookup"><span data-stu-id="932a8-127">-Confirm</span></span>
<span data-ttu-id="932a8-128">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="932a8-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="932a8-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="932a8-129">-WhatIf</span></span>
<span data-ttu-id="932a8-130">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="932a8-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="932a8-131">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="932a8-131">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="932a8-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="932a8-132">CommonParameters</span></span>
<span data-ttu-id="932a8-133">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="932a8-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="932a8-134">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="932a8-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="932a8-135">입력</span><span class="sxs-lookup"><span data-stu-id="932a8-135">INPUTS</span></span>

### <span data-ttu-id="932a8-136">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="932a8-136">System.String</span></span>

## <span data-ttu-id="932a8-137">출력</span><span class="sxs-lookup"><span data-stu-id="932a8-137">OUTPUTS</span></span>

### <span data-ttu-id="932a8-138">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="932a8-138">System.Boolean</span></span>

## <span data-ttu-id="932a8-139">상속자</span><span class="sxs-lookup"><span data-stu-id="932a8-139">NOTES</span></span>

## <span data-ttu-id="932a8-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="932a8-140">RELATED LINKS</span></span>

[<span data-ttu-id="932a8-141">Get-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="932a8-141">Get-AzResourceGroupDeployment</span></span>](./Get-AzResourceGroupDeployment.md)

[<span data-ttu-id="932a8-142">새로운 AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="932a8-142">New-AzResourceGroupDeployment</span></span>](./New-AzResourceGroupDeployment.md)

[<span data-ttu-id="932a8-143">중지-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="932a8-143">Stop-AzResourceGroupDeployment</span></span>](./Stop-AzResourceGroupDeployment.md)

[<span data-ttu-id="932a8-144">테스트-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="932a8-144">Test-AzResourceGroupDeployment</span></span>](./Test-AzResourceGroupDeployment.md)


