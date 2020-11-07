---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: C3DD193E-B8FE-468D-BEE7-00C3D99B469E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/remove-azurermresourcegroupdeployment
schema: 2.0.0
ms.openlocfilehash: bfe0bad0104708e635b49f02cfb1eecd2474ea5b
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93882769"
---
# <span data-ttu-id="287d6-101">Remove-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="287d6-101">Remove-AzureRmResourceGroupDeployment</span></span>

## <span data-ttu-id="287d6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="287d6-102">SYNOPSIS</span></span>
<span data-ttu-id="287d6-103">리소스 그룹 배포 및 연결 된 작업을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="287d6-103">Removes a resource group deployment and any associated operations.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="287d6-104">구문과</span><span class="sxs-lookup"><span data-stu-id="287d6-104">SYNTAX</span></span>

### <span data-ttu-id="287d6-105">RemoveByResourceGroupName (기본값)</span><span class="sxs-lookup"><span data-stu-id="287d6-105">RemoveByResourceGroupName (Default)</span></span>
```
Remove-AzureRmResourceGroupDeployment -ResourceGroupName <String> -Name <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="287d6-106">RemoveByResourceGroupDeploymentId</span><span class="sxs-lookup"><span data-stu-id="287d6-106">RemoveByResourceGroupDeploymentId</span></span>
```
Remove-AzureRmResourceGroupDeployment -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="287d6-107">설명은</span><span class="sxs-lookup"><span data-stu-id="287d6-107">DESCRIPTION</span></span>
<span data-ttu-id="287d6-108">**AzureRmResourceGroupDeployment** Cmdlet은 Azure 리소스 그룹 배포 및 연결 된 작업을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="287d6-108">The **Remove-AzureRmResourceGroupDeployment** cmdlet removes an Azure resource group deployment and any associated operations.</span></span>

## <span data-ttu-id="287d6-109">예제의</span><span class="sxs-lookup"><span data-stu-id="287d6-109">EXAMPLES</span></span>

## <span data-ttu-id="287d6-110">변수</span><span class="sxs-lookup"><span data-stu-id="287d6-110">PARAMETERS</span></span>

### <span data-ttu-id="287d6-111">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="287d6-111">-ApiVersion</span></span>
<span data-ttu-id="287d6-112">리소스 공급자가 지 원하는 API 버전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="287d6-112">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="287d6-113">기본 버전 외의 다른 버전을 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="287d6-113">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="287d6-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="287d6-114">-DefaultProfile</span></span>
<span data-ttu-id="287d6-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="287d6-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="287d6-116">-Id</span><span class="sxs-lookup"><span data-stu-id="287d6-116">-Id</span></span>
<span data-ttu-id="287d6-117">제거할 리소스 그룹 배포의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="287d6-117">Specifies the ID of the resource group deployment to remove.</span></span>

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

### <span data-ttu-id="287d6-118">-이름</span><span class="sxs-lookup"><span data-stu-id="287d6-118">-Name</span></span>
<span data-ttu-id="287d6-119">제거할 리소스 그룹 배포의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="287d6-119">Specifies the name of the resource group deployment to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByResourceGroupName
Aliases: DeploymentName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="287d6-120">-Pre</span><span class="sxs-lookup"><span data-stu-id="287d6-120">-Pre</span></span>
<span data-ttu-id="287d6-121">이 cmdlet이 사용할 버전을 자동으로 결정 하는 경우 시험판 API 버전을 고려 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="287d6-121">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="287d6-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="287d6-122">-ResourceGroupName</span></span>
<span data-ttu-id="287d6-123">제거할 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="287d6-123">Specifies the name of the resource group to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByResourceGroupName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="287d6-124">-확인</span><span class="sxs-lookup"><span data-stu-id="287d6-124">-Confirm</span></span>
<span data-ttu-id="287d6-125">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="287d6-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="287d6-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="287d6-126">-WhatIf</span></span>
<span data-ttu-id="287d6-127">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="287d6-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="287d6-128">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="287d6-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="287d6-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="287d6-129">CommonParameters</span></span>
<span data-ttu-id="287d6-130">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="287d6-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="287d6-131">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="287d6-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="287d6-132">입력</span><span class="sxs-lookup"><span data-stu-id="287d6-132">INPUTS</span></span>

### <span data-ttu-id="287d6-133">않아야</span><span class="sxs-lookup"><span data-stu-id="287d6-133">None</span></span>

## <span data-ttu-id="287d6-134">출력</span><span class="sxs-lookup"><span data-stu-id="287d6-134">OUTPUTS</span></span>

## <span data-ttu-id="287d6-135">상속자</span><span class="sxs-lookup"><span data-stu-id="287d6-135">NOTES</span></span>

## <span data-ttu-id="287d6-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="287d6-136">RELATED LINKS</span></span>

[<span data-ttu-id="287d6-137">Get-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="287d6-137">Get-AzureRmResourceGroupDeployment</span></span>](./Get-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="287d6-138">새로운 AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="287d6-138">New-AzureRmResourceGroupDeployment</span></span>](./New-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="287d6-139">중지-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="287d6-139">Stop-AzureRmResourceGroupDeployment</span></span>](./Stop-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="287d6-140">테스트-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="287d6-140">Test-AzureRmResourceGroupDeployment</span></span>](./Test-AzureRmResourceGroupDeployment.md)


