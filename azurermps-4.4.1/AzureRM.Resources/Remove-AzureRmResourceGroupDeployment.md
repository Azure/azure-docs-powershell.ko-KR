---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: C3DD193E-B8FE-468D-BEE7-00C3D99B469E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmResourceGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmResourceGroupDeployment.md
ms.openlocfilehash: 84aa6f50d02f4c85de674c163565a205f2b83750
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93532944"
---
# <span data-ttu-id="77a76-101">Remove-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="77a76-101">Remove-AzureRmResourceGroupDeployment</span></span>

## <span data-ttu-id="77a76-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="77a76-102">SYNOPSIS</span></span>
<span data-ttu-id="77a76-103">리소스 그룹 배포 및 연결 된 작업을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="77a76-103">Removes a resource group deployment and any associated operations.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="77a76-104">구문과</span><span class="sxs-lookup"><span data-stu-id="77a76-104">SYNTAX</span></span>

### <span data-ttu-id="77a76-105">배포 이름 매개 변수 집합</span><span class="sxs-lookup"><span data-stu-id="77a76-105">The deployment name parameter set.</span></span> <span data-ttu-id="77a76-106">기본값</span><span class="sxs-lookup"><span data-stu-id="77a76-106">(Default)</span></span>
```
Remove-AzureRmResourceGroupDeployment -ResourceGroupName <String> -Name <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="77a76-107">배포 Id 매개 변수 집합</span><span class="sxs-lookup"><span data-stu-id="77a76-107">The deployment Id parameter set.</span></span>
```
Remove-AzureRmResourceGroupDeployment -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="77a76-108">설명은</span><span class="sxs-lookup"><span data-stu-id="77a76-108">DESCRIPTION</span></span>
<span data-ttu-id="77a76-109">**AzureRmResourceGroupDeployment** Cmdlet은 Azure 리소스 그룹 배포 및 연결 된 작업을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="77a76-109">The **Remove-AzureRmResourceGroupDeployment** cmdlet removes an Azure resource group deployment and any associated operations.</span></span>

## <span data-ttu-id="77a76-110">예제의</span><span class="sxs-lookup"><span data-stu-id="77a76-110">EXAMPLES</span></span>

## <span data-ttu-id="77a76-111">변수</span><span class="sxs-lookup"><span data-stu-id="77a76-111">PARAMETERS</span></span>

### <span data-ttu-id="77a76-112">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="77a76-112">-ApiVersion</span></span>
<span data-ttu-id="77a76-113">리소스 공급자가 지 원하는 API 버전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="77a76-113">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="77a76-114">기본 버전 외의 다른 버전을 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="77a76-114">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="77a76-115">-Id</span><span class="sxs-lookup"><span data-stu-id="77a76-115">-Id</span></span>
<span data-ttu-id="77a76-116">제거할 리소스 그룹 배포의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="77a76-116">Specifies the ID of the resource group deployment to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: The deployment Id parameter set.
Aliases: DeploymentId, ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77a76-117">-이름</span><span class="sxs-lookup"><span data-stu-id="77a76-117">-Name</span></span>
<span data-ttu-id="77a76-118">제거할 리소스 그룹 배포의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="77a76-118">Specifies the name of the resource group deployment to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: The deployment name parameter set.
Aliases: DeploymentName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="77a76-119">-Pre</span><span class="sxs-lookup"><span data-stu-id="77a76-119">-Pre</span></span>
<span data-ttu-id="77a76-120">이 cmdlet이 사용할 버전을 자동으로 결정 하는 경우 시험판 API 버전을 고려 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="77a76-120">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="77a76-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="77a76-121">-ResourceGroupName</span></span>
<span data-ttu-id="77a76-122">제거할 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="77a76-122">Specifies the name of the resource group to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: The deployment name parameter set.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="77a76-123">-확인</span><span class="sxs-lookup"><span data-stu-id="77a76-123">-Confirm</span></span>
<span data-ttu-id="77a76-124">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="77a76-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="77a76-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="77a76-125">-WhatIf</span></span>
<span data-ttu-id="77a76-126">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="77a76-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="77a76-127">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="77a76-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="77a76-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="77a76-128">-DefaultProfile</span></span>
<span data-ttu-id="77a76-129">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="77a76-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="77a76-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="77a76-130">CommonParameters</span></span>
<span data-ttu-id="77a76-131">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="77a76-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="77a76-132">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="77a76-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="77a76-133">입력</span><span class="sxs-lookup"><span data-stu-id="77a76-133">INPUTS</span></span>

## <span data-ttu-id="77a76-134">출력</span><span class="sxs-lookup"><span data-stu-id="77a76-134">OUTPUTS</span></span>

### <span data-ttu-id="77a76-135">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="77a76-135">System.Boolean</span></span>

## <span data-ttu-id="77a76-136">상속자</span><span class="sxs-lookup"><span data-stu-id="77a76-136">NOTES</span></span>

## <span data-ttu-id="77a76-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="77a76-137">RELATED LINKS</span></span>

[<span data-ttu-id="77a76-138">Get-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="77a76-138">Get-AzureRmResourceGroupDeployment</span></span>](./Get-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="77a76-139">새로운 AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="77a76-139">New-AzureRmResourceGroupDeployment</span></span>](./New-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="77a76-140">중지-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="77a76-140">Stop-AzureRmResourceGroupDeployment</span></span>](./Stop-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="77a76-141">테스트-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="77a76-141">Test-AzureRmResourceGroupDeployment</span></span>](./Test-AzureRmResourceGroupDeployment.md)

