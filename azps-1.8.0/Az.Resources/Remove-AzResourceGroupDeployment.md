---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: C3DD193E-B8FE-468D-BEE7-00C3D99B469E
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azresourcegroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzResourceGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzResourceGroupDeployment.md
ms.openlocfilehash: 2cae601904b15e2508886374c1b607ed8aec4b93
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93699332"
---
# <span data-ttu-id="ccb0b-101">Remove-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="ccb0b-101">Remove-AzResourceGroupDeployment</span></span>

## <span data-ttu-id="ccb0b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ccb0b-102">SYNOPSIS</span></span>
<span data-ttu-id="ccb0b-103">리소스 그룹 배포 및 연결 된 작업을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="ccb0b-103">Removes a resource group deployment and any associated operations.</span></span>

## <span data-ttu-id="ccb0b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ccb0b-104">SYNTAX</span></span>

### <span data-ttu-id="ccb0b-105">RemoveByResourceGroupName (기본값)</span><span class="sxs-lookup"><span data-stu-id="ccb0b-105">RemoveByResourceGroupName (Default)</span></span>
```
Remove-AzResourceGroupDeployment [-ResourceGroupName] <String> [-Name] <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ccb0b-106">RemoveByResourceGroupDeploymentId</span><span class="sxs-lookup"><span data-stu-id="ccb0b-106">RemoveByResourceGroupDeploymentId</span></span>
```
Remove-AzResourceGroupDeployment -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ccb0b-107">설명은</span><span class="sxs-lookup"><span data-stu-id="ccb0b-107">DESCRIPTION</span></span>
<span data-ttu-id="ccb0b-108">**AzResourceGroupDeployment** Cmdlet은 Azure 리소스 그룹 배포 및 연결 된 작업을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="ccb0b-108">The **Remove-AzResourceGroupDeployment** cmdlet removes an Azure resource group deployment and any associated operations.</span></span>

## <span data-ttu-id="ccb0b-109">예제의</span><span class="sxs-lookup"><span data-stu-id="ccb0b-109">EXAMPLES</span></span>

## <span data-ttu-id="ccb0b-110">변수</span><span class="sxs-lookup"><span data-stu-id="ccb0b-110">PARAMETERS</span></span>

### <span data-ttu-id="ccb0b-111">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="ccb0b-111">-ApiVersion</span></span>
<span data-ttu-id="ccb0b-112">리소스 공급자가 지 원하는 API 버전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ccb0b-112">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="ccb0b-113">기본 버전 외의 다른 버전을 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ccb0b-113">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="ccb0b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ccb0b-114">-DefaultProfile</span></span>
<span data-ttu-id="ccb0b-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="ccb0b-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ccb0b-116">-Id</span><span class="sxs-lookup"><span data-stu-id="ccb0b-116">-Id</span></span>
<span data-ttu-id="ccb0b-117">제거할 리소스 그룹 배포의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ccb0b-117">Specifies the ID of the resource group deployment to remove.</span></span>

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

### <span data-ttu-id="ccb0b-118">-이름</span><span class="sxs-lookup"><span data-stu-id="ccb0b-118">-Name</span></span>
<span data-ttu-id="ccb0b-119">제거할 리소스 그룹 배포의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ccb0b-119">Specifies the name of the resource group deployment to remove.</span></span>

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

### <span data-ttu-id="ccb0b-120">-Pre</span><span class="sxs-lookup"><span data-stu-id="ccb0b-120">-Pre</span></span>
<span data-ttu-id="ccb0b-121">이 cmdlet이 사용할 버전을 자동으로 결정 하는 경우 시험판 API 버전을 고려 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="ccb0b-121">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="ccb0b-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ccb0b-122">-ResourceGroupName</span></span>
<span data-ttu-id="ccb0b-123">제거할 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ccb0b-123">Specifies the name of the resource group to remove.</span></span>

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

### <span data-ttu-id="ccb0b-124">-확인</span><span class="sxs-lookup"><span data-stu-id="ccb0b-124">-Confirm</span></span>
<span data-ttu-id="ccb0b-125">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="ccb0b-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ccb0b-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ccb0b-126">-WhatIf</span></span>
<span data-ttu-id="ccb0b-127">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="ccb0b-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ccb0b-128">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ccb0b-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ccb0b-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ccb0b-129">CommonParameters</span></span>
<span data-ttu-id="ccb0b-130">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ccb0b-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ccb0b-131">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ccb0b-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ccb0b-132">입력</span><span class="sxs-lookup"><span data-stu-id="ccb0b-132">INPUTS</span></span>

### <span data-ttu-id="ccb0b-133">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="ccb0b-133">System.String</span></span>

## <span data-ttu-id="ccb0b-134">출력</span><span class="sxs-lookup"><span data-stu-id="ccb0b-134">OUTPUTS</span></span>

### <span data-ttu-id="ccb0b-135">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="ccb0b-135">System.Boolean</span></span>

## <span data-ttu-id="ccb0b-136">상속자</span><span class="sxs-lookup"><span data-stu-id="ccb0b-136">NOTES</span></span>

## <span data-ttu-id="ccb0b-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ccb0b-137">RELATED LINKS</span></span>

[<span data-ttu-id="ccb0b-138">Get-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="ccb0b-138">Get-AzResourceGroupDeployment</span></span>](./Get-AzResourceGroupDeployment.md)

[<span data-ttu-id="ccb0b-139">새로운 AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="ccb0b-139">New-AzResourceGroupDeployment</span></span>](./New-AzResourceGroupDeployment.md)

[<span data-ttu-id="ccb0b-140">중지-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="ccb0b-140">Stop-AzResourceGroupDeployment</span></span>](./Stop-AzResourceGroupDeployment.md)

[<span data-ttu-id="ccb0b-141">테스트-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="ccb0b-141">Test-AzResourceGroupDeployment</span></span>](./Test-AzResourceGroupDeployment.md)


