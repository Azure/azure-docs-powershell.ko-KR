---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: C3DD193E-B8FE-468D-BEE7-00C3D99B469E
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azresourcegroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzResourceGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzResourceGroupDeployment.md
ms.openlocfilehash: c504a839b47fc36863e207f74d9b309309a31fbb
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94204406"
---
# <span data-ttu-id="8e95a-101">Remove-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="8e95a-101">Remove-AzResourceGroupDeployment</span></span>

## <span data-ttu-id="8e95a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8e95a-102">SYNOPSIS</span></span>
<span data-ttu-id="8e95a-103">리소스 그룹 배포 및 연결 된 작업을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="8e95a-103">Removes a resource group deployment and any associated operations.</span></span>

## <span data-ttu-id="8e95a-104">구문과</span><span class="sxs-lookup"><span data-stu-id="8e95a-104">SYNTAX</span></span>

### <span data-ttu-id="8e95a-105">RemoveByResourceGroupName (기본값)</span><span class="sxs-lookup"><span data-stu-id="8e95a-105">RemoveByResourceGroupName (Default)</span></span>
```
Remove-AzResourceGroupDeployment [-ResourceGroupName] <String> [-Name] <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8e95a-106">RemoveByResourceGroupDeploymentId</span><span class="sxs-lookup"><span data-stu-id="8e95a-106">RemoveByResourceGroupDeploymentId</span></span>
```
Remove-AzResourceGroupDeployment -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8e95a-107">설명은</span><span class="sxs-lookup"><span data-stu-id="8e95a-107">DESCRIPTION</span></span>

<span data-ttu-id="8e95a-108">**AzResourceGroupDeployment** Cmdlet은 Azure 리소스 그룹 배포 및 연결 된 작업을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="8e95a-108">The **Remove-AzResourceGroupDeployment** cmdlet removes an Azure resource group deployment and any associated operations.</span></span>

## <span data-ttu-id="8e95a-109">예제의</span><span class="sxs-lookup"><span data-stu-id="8e95a-109">EXAMPLES</span></span>

### <span data-ttu-id="8e95a-110">예제 1: ResourceId를 사용 하 여 리소스 그룹 배포 제거</span><span class="sxs-lookup"><span data-stu-id="8e95a-110">Example 1: Removes a resource group deployment with ResourceId</span></span>

```powershell
PS C:\>Remove-AzResourceGroupDeployment -ResourceId /subscriptions/{subId}/resourceGroups/testGroup/providers/Microsoft.Resources/deployments/testDeployment1

True
```

<span data-ttu-id="8e95a-111">이 명령은 배포의 정규화 된 리소스 Id를 사용 하 여 리소스 그룹 배포를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="8e95a-111">This command removes a resource group deployment with the fully qualified resource Id of the deployment.</span></span>
<span data-ttu-id="8e95a-112">성공적으로 제거 되 면 true를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="8e95a-112">Successful removal returns true.</span></span>

### <span data-ttu-id="8e95a-113">예제 2: ResourceGroupName 및 Context.resourcename을 사용 하 여 리소스 그룹 배포 제거</span><span class="sxs-lookup"><span data-stu-id="8e95a-113">Example 2: Removes a resource group deployment with ResourceGroupName and ResourceName</span></span>

```powershell
PS C:\>Remove-AzResourceGroupDeployment -ResourceGroupName testGroup -Name testDeployment1

True
```

<span data-ttu-id="8e95a-114">이 명령은 제공 된 ResourceGroupName 및 Context.resourcename을 사용 하 여 리소스 그룹 배포를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="8e95a-114">This command removes a resource group deployment with the provided ResourceGroupName and ResourceName.</span></span>
<span data-ttu-id="8e95a-115">성공적으로 제거 되 면 true를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="8e95a-115">Successful removal returns true.</span></span>

## <span data-ttu-id="8e95a-116">변수</span><span class="sxs-lookup"><span data-stu-id="8e95a-116">PARAMETERS</span></span>

### <span data-ttu-id="8e95a-117">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="8e95a-117">-ApiVersion</span></span>
<span data-ttu-id="8e95a-118">리소스 공급자가 지 원하는 API 버전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8e95a-118">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="8e95a-119">기본 버전 외의 다른 버전을 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8e95a-119">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="8e95a-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e95a-120">-DefaultProfile</span></span>
<span data-ttu-id="8e95a-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="8e95a-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8e95a-122">-Id</span><span class="sxs-lookup"><span data-stu-id="8e95a-122">-Id</span></span>
<span data-ttu-id="8e95a-123">제거할 리소스 그룹 배포의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8e95a-123">Specifies the ID of the resource group deployment to remove.</span></span>

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

### <span data-ttu-id="8e95a-124">-이름</span><span class="sxs-lookup"><span data-stu-id="8e95a-124">-Name</span></span>
<span data-ttu-id="8e95a-125">제거할 리소스 그룹 배포의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8e95a-125">Specifies the name of the resource group deployment to remove.</span></span>

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

### <span data-ttu-id="8e95a-126">-Pre</span><span class="sxs-lookup"><span data-stu-id="8e95a-126">-Pre</span></span>
<span data-ttu-id="8e95a-127">이 cmdlet이 사용할 버전을 자동으로 결정 하는 경우 시험판 API 버전을 고려 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="8e95a-127">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="8e95a-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8e95a-128">-ResourceGroupName</span></span>
<span data-ttu-id="8e95a-129">제거할 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8e95a-129">Specifies the name of the resource group to remove.</span></span>

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

### <span data-ttu-id="8e95a-130">-확인</span><span class="sxs-lookup"><span data-stu-id="8e95a-130">-Confirm</span></span>
<span data-ttu-id="8e95a-131">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="8e95a-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8e95a-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8e95a-132">-WhatIf</span></span>
<span data-ttu-id="8e95a-133">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="8e95a-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8e95a-134">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="8e95a-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8e95a-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e95a-135">CommonParameters</span></span>
<span data-ttu-id="8e95a-136">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="8e95a-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e95a-137">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="8e95a-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e95a-138">입력</span><span class="sxs-lookup"><span data-stu-id="8e95a-138">INPUTS</span></span>

### <span data-ttu-id="8e95a-139">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="8e95a-139">System.String</span></span>

## <span data-ttu-id="8e95a-140">출력</span><span class="sxs-lookup"><span data-stu-id="8e95a-140">OUTPUTS</span></span>

### <span data-ttu-id="8e95a-141">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="8e95a-141">System.Boolean</span></span>

## <span data-ttu-id="8e95a-142">상속자</span><span class="sxs-lookup"><span data-stu-id="8e95a-142">NOTES</span></span>

## <span data-ttu-id="8e95a-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8e95a-143">RELATED LINKS</span></span>

[<span data-ttu-id="8e95a-144">Get-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="8e95a-144">Get-AzResourceGroupDeployment</span></span>](./Get-AzResourceGroupDeployment.md)

[<span data-ttu-id="8e95a-145">새로운 AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="8e95a-145">New-AzResourceGroupDeployment</span></span>](./New-AzResourceGroupDeployment.md)

[<span data-ttu-id="8e95a-146">중지-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="8e95a-146">Stop-AzResourceGroupDeployment</span></span>](./Stop-AzResourceGroupDeployment.md)

[<span data-ttu-id="8e95a-147">테스트-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="8e95a-147">Test-AzResourceGroupDeployment</span></span>](./Test-AzResourceGroupDeployment.md)


