---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 089954C3-7F3E-46C2-AA93-C0151EACDA2F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Stop-AzureRmResourceGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Stop-AzureRmResourceGroupDeployment.md
ms.openlocfilehash: f07b2f59f1a38aca780e1e869bb3904725df6dcd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93711495"
---
# <span data-ttu-id="23cf7-101">Stop-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="23cf7-101">Stop-AzureRmResourceGroupDeployment</span></span>

## <span data-ttu-id="23cf7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="23cf7-102">SYNOPSIS</span></span>
<span data-ttu-id="23cf7-103">리소스 그룹 배포를 취소 합니다.</span><span class="sxs-lookup"><span data-stu-id="23cf7-103">Cancels a resource group deployment.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="23cf7-104">구문과</span><span class="sxs-lookup"><span data-stu-id="23cf7-104">SYNTAX</span></span>

### <span data-ttu-id="23cf7-105">배포 이름 매개 변수 집합</span><span class="sxs-lookup"><span data-stu-id="23cf7-105">The deployment name parameter set.</span></span> <span data-ttu-id="23cf7-106">기본값</span><span class="sxs-lookup"><span data-stu-id="23cf7-106">(Default)</span></span>
```
Stop-AzureRmResourceGroupDeployment [-ResourceGroupName] <String> [-Name] <String> [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="23cf7-107">배포 Id 매개 변수 집합</span><span class="sxs-lookup"><span data-stu-id="23cf7-107">The deployment Id parameter set.</span></span>
```
Stop-AzureRmResourceGroupDeployment -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="23cf7-108">설명은</span><span class="sxs-lookup"><span data-stu-id="23cf7-108">DESCRIPTION</span></span>
<span data-ttu-id="23cf7-109">**AzureRmResourceGroupDeployment** cmdlet은 시작 되었지만 완료 되지 않은 Azure 리소스 그룹 배포를 취소 합니다.</span><span class="sxs-lookup"><span data-stu-id="23cf7-109">The **Stop-AzureRmResourceGroupDeployment** cmdlet cancels an Azure resource group deployment that has started but not completed.</span></span>
<span data-ttu-id="23cf7-110">배포를 중지 하려면 배포에는 프로비저닝 등의 완료 되지 않은 상태 (예: 프로 비전 됨 또는 실패)가 아닌 완전 한 프로비저닝 상태가 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="23cf7-110">To stop a deployment, the deployment must have an incomplete provisioning state, such as Provisioning, and not a completed state, such as Provisioned or Failed.</span></span>

<span data-ttu-id="23cf7-111">Azure 리소스는 웹 사이트, 데이터베이스 또는 데이터베이스 서버와 같이 사용자가 관리 하는 엔터티입니다.</span><span class="sxs-lookup"><span data-stu-id="23cf7-111">An Azure resource is a user-managed entity, such as a website, database, or database server.</span></span>
<span data-ttu-id="23cf7-112">리소스 그룹은 하나의 단위로 배포 되는 리소스 모음입니다.</span><span class="sxs-lookup"><span data-stu-id="23cf7-112">A resource group is a collection of resources that are deployed as a unit.</span></span>
<span data-ttu-id="23cf7-113">리소스 그룹을 배포 하려면 New-AzureRmResourceGroupDeployment cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="23cf7-113">To deploy a resource group, use the New-AzureRmResourceGroupDeployment cmdlet.</span></span>

<span data-ttu-id="23cf7-114">New-AzureRmResource cmdlet은 새 리소스를 만들지만이 cmdlet이 중지할 수 있는 리소스 그룹 배포 작업을 트리거하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="23cf7-114">The New-AzureRmResource cmdlet creates a new resource, but it does not trigger a resource group deployment operation that this cmdlet can stop.</span></span>
<span data-ttu-id="23cf7-115">이 cmdlet는 실행 중인 하나의 배포만 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="23cf7-115">This cmdlet stops only one running deployment.</span></span>

<span data-ttu-id="23cf7-116">특정 배포를 중지 하려면 *Name* 매개 변수를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="23cf7-116">Use the *Name* parameter to stop a specific deployment.</span></span>
<span data-ttu-id="23cf7-117">*Name* 매개 변수를 생략 하면 **AzureRmResourceGroupDeployment** 는 실행 중인 배포를 검색 하 고 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="23cf7-117">If you omit the *Name* parameter, **Stop-AzureRmResourceGroupDeployment** searches for a running deployment and stops it.</span></span>
<span data-ttu-id="23cf7-118">Cmdlet이 실행 중인 배포를 두 개 이상 찾으면 명령이 실패 합니다.</span><span class="sxs-lookup"><span data-stu-id="23cf7-118">If the cmdlet finds more than one running deployment, the command fails.</span></span>

## <span data-ttu-id="23cf7-119">예제의</span><span class="sxs-lookup"><span data-stu-id="23cf7-119">EXAMPLES</span></span>

## <span data-ttu-id="23cf7-120">변수</span><span class="sxs-lookup"><span data-stu-id="23cf7-120">PARAMETERS</span></span>

### <span data-ttu-id="23cf7-121">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="23cf7-121">-ApiVersion</span></span>
<span data-ttu-id="23cf7-122">리소스 공급자가 지 원하는 API 버전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="23cf7-122">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="23cf7-123">기본 버전 외의 다른 버전을 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="23cf7-123">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="23cf7-124">-Id</span><span class="sxs-lookup"><span data-stu-id="23cf7-124">-Id</span></span>
<span data-ttu-id="23cf7-125">중지할 리소스 그룹 배포의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="23cf7-125">Specifies the ID of the resource group deployment to stop.</span></span>

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

### <span data-ttu-id="23cf7-126">-이름</span><span class="sxs-lookup"><span data-stu-id="23cf7-126">-Name</span></span>
<span data-ttu-id="23cf7-127">중지할 리소스 그룹 배포의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="23cf7-127">Specifies the name of the resource group deployment to stop.</span></span>

<span data-ttu-id="23cf7-128">이 매개 변수를 지정 하지 않으면이 cmdlet이 리소스 그룹에서 실행 중인 배포를 검색 하 고 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="23cf7-128">If you do not specify this parameter, this cmdlet searches for a running deployment in the resource group and stops it.</span></span>
<span data-ttu-id="23cf7-129">실행 중인 배포를 두 개 이상 찾으면 명령이 실패 합니다.</span><span class="sxs-lookup"><span data-stu-id="23cf7-129">If it finds more than one running deployment, the command fails.</span></span>
<span data-ttu-id="23cf7-130">배포 이름을 가져오려면 Get-AzureRmResourceGroupDeployment cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="23cf7-130">To get the deployment name, use the Get-AzureRmResourceGroupDeployment cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: The deployment name parameter set.
Aliases: DeploymentName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="23cf7-131">-Pre</span><span class="sxs-lookup"><span data-stu-id="23cf7-131">-Pre</span></span>
<span data-ttu-id="23cf7-132">이 cmdlet이 사용할 버전을 자동으로 결정 하는 경우 시험판 API 버전을 고려 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="23cf7-132">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="23cf7-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="23cf7-133">-ResourceGroupName</span></span>
<span data-ttu-id="23cf7-134">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="23cf7-134">Specifies the name of the resource group.</span></span>
<span data-ttu-id="23cf7-135">이 cmdlet은이 매개 변수에서 지정 하는 리소스 그룹의 배포를 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="23cf7-135">This cmdlet stops the deployment of the resource group that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: The deployment name parameter set.
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="23cf7-136">-확인</span><span class="sxs-lookup"><span data-stu-id="23cf7-136">-Confirm</span></span>
<span data-ttu-id="23cf7-137">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="23cf7-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="23cf7-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="23cf7-138">-WhatIf</span></span>
<span data-ttu-id="23cf7-139">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="23cf7-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="23cf7-140">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="23cf7-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="23cf7-141">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23cf7-141">-DefaultProfile</span></span>
<span data-ttu-id="23cf7-142">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="23cf7-142">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="23cf7-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23cf7-143">CommonParameters</span></span>
<span data-ttu-id="23cf7-144">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="23cf7-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23cf7-145">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="23cf7-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23cf7-146">입력</span><span class="sxs-lookup"><span data-stu-id="23cf7-146">INPUTS</span></span>

### <span data-ttu-id="23cf7-147">않아야</span><span class="sxs-lookup"><span data-stu-id="23cf7-147">None</span></span>

## <span data-ttu-id="23cf7-148">출력</span><span class="sxs-lookup"><span data-stu-id="23cf7-148">OUTPUTS</span></span>

### <span data-ttu-id="23cf7-149">나타내는</span><span class="sxs-lookup"><span data-stu-id="23cf7-149">Boolean</span></span>

## <span data-ttu-id="23cf7-150">상속자</span><span class="sxs-lookup"><span data-stu-id="23cf7-150">NOTES</span></span>

## <span data-ttu-id="23cf7-151">관련 링크</span><span class="sxs-lookup"><span data-stu-id="23cf7-151">RELATED LINKS</span></span>

[<span data-ttu-id="23cf7-152">Get-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="23cf7-152">Get-AzureRmResourceGroupDeployment</span></span>](./Get-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="23cf7-153">새로운 AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="23cf7-153">New-AzureRmResource</span></span>](./New-AzureRmResource.md)

[<span data-ttu-id="23cf7-154">새로운 AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="23cf7-154">New-AzureRmResourceGroup</span></span>](./New-AzureRmResourceGroup.md)

[<span data-ttu-id="23cf7-155">새로운 AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="23cf7-155">New-AzureRmResourceGroupDeployment</span></span>](./New-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="23cf7-156">제거-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="23cf7-156">Remove-AzureRmResourceGroupDeployment</span></span>](./Remove-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="23cf7-157">테스트-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="23cf7-157">Test-AzureRmResourceGroupDeployment</span></span>](./Test-AzureRmResourceGroupDeployment.md)


