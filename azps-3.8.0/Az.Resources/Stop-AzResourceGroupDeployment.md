---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 089954C3-7F3E-46C2-AA93-C0151EACDA2F
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/stop-azresourcegroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Stop-AzResourceGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Stop-AzResourceGroupDeployment.md
ms.openlocfilehash: 01f2aa36a063caec233aa8c1600d4a01727a549b
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94041711"
---
# <span data-ttu-id="9274f-101">Stop-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="9274f-101">Stop-AzResourceGroupDeployment</span></span>

## <span data-ttu-id="9274f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9274f-102">SYNOPSIS</span></span>
<span data-ttu-id="9274f-103">리소스 그룹 배포를 취소 합니다.</span><span class="sxs-lookup"><span data-stu-id="9274f-103">Cancels a resource group deployment.</span></span>

## <span data-ttu-id="9274f-104">구문과</span><span class="sxs-lookup"><span data-stu-id="9274f-104">SYNTAX</span></span>

### <span data-ttu-id="9274f-105">StopByResourceGroupDeploymentName (기본값)</span><span class="sxs-lookup"><span data-stu-id="9274f-105">StopByResourceGroupDeploymentName (Default)</span></span>
```
Stop-AzResourceGroupDeployment [-ResourceGroupName] <String> [-Name] <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9274f-106">StopByResourceGroupDeploymentId</span><span class="sxs-lookup"><span data-stu-id="9274f-106">StopByResourceGroupDeploymentId</span></span>
```
Stop-AzResourceGroupDeployment -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9274f-107">설명은</span><span class="sxs-lookup"><span data-stu-id="9274f-107">DESCRIPTION</span></span>
<span data-ttu-id="9274f-108">**AzResourceGroupDeployment** cmdlet은 시작 되었지만 완료 되지 않은 Azure 리소스 그룹 배포를 취소 합니다.</span><span class="sxs-lookup"><span data-stu-id="9274f-108">The **Stop-AzResourceGroupDeployment** cmdlet cancels an Azure resource group deployment that has started but not completed.</span></span>
<span data-ttu-id="9274f-109">배포를 중지 하려면 배포에는 프로비저닝 등의 완료 되지 않은 상태 (예: 프로 비전 됨 또는 실패)가 아닌 완전 한 프로비저닝 상태가 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="9274f-109">To stop a deployment, the deployment must have an incomplete provisioning state, such as Provisioning, and not a completed state, such as Provisioned or Failed.</span></span>
<span data-ttu-id="9274f-110">Azure 리소스는 웹 사이트, 데이터베이스 또는 데이터베이스 서버와 같이 사용자가 관리 하는 엔터티입니다.</span><span class="sxs-lookup"><span data-stu-id="9274f-110">An Azure resource is a user-managed entity, such as a website, database, or database server.</span></span>
<span data-ttu-id="9274f-111">리소스 그룹은 하나의 단위로 배포 되는 리소스 모음입니다.</span><span class="sxs-lookup"><span data-stu-id="9274f-111">A resource group is a collection of resources that are deployed as a unit.</span></span>
<span data-ttu-id="9274f-112">리소스 그룹을 배포 하려면 New-AzResourceGroupDeployment cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="9274f-112">To deploy a resource group, use the New-AzResourceGroupDeployment cmdlet.</span></span>
<span data-ttu-id="9274f-113">New-AzResource cmdlet은 새 리소스를 만들지만이 cmdlet이 중지할 수 있는 리소스 그룹 배포 작업을 트리거하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9274f-113">The New-AzResource cmdlet creates a new resource, but it does not trigger a resource group deployment operation that this cmdlet can stop.</span></span>
<span data-ttu-id="9274f-114">이 cmdlet는 실행 중인 하나의 배포만 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="9274f-114">This cmdlet stops only one running deployment.</span></span>
<span data-ttu-id="9274f-115">특정 배포를 중지 하려면 *Name* 매개 변수를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="9274f-115">Use the *Name* parameter to stop a specific deployment.</span></span>
<span data-ttu-id="9274f-116">*Name* 매개 변수를 생략 하면 **AzResourceGroupDeployment** 는 실행 중인 배포를 검색 하 고 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="9274f-116">If you omit the *Name* parameter, **Stop-AzResourceGroupDeployment** searches for a running deployment and stops it.</span></span>
<span data-ttu-id="9274f-117">Cmdlet이 실행 중인 배포를 두 개 이상 찾으면 명령이 실패 합니다.</span><span class="sxs-lookup"><span data-stu-id="9274f-117">If the cmdlet finds more than one running deployment, the command fails.</span></span>

## <span data-ttu-id="9274f-118">예제의</span><span class="sxs-lookup"><span data-stu-id="9274f-118">EXAMPLES</span></span>

### <span data-ttu-id="9274f-119">예제 1: 리소스 그룹 배포 시작 및 중지</span><span class="sxs-lookup"><span data-stu-id="9274f-119">Example 1: Starting and stopping a resource group deployment</span></span>

```powershell
PS C:\> New-AzResourceGroupDeployment -Name mynewstorageaccount -ResourceGroupName myrg -TemplateFile .\storage-account-create-azdeploy.json -TemplateParameterFile .\storage-account-create-azdeploy.parameters.json -AsJob

Id     Name            PSJobTypeName   State         HasMoreData     Location             Command
--     ----            -------------   -----         -----------     --------             -------
1      Long Running... AzureLongRun... Running       True            localhost            New-AzResourceGro...

PS C:\> Stop-AzResourceGroupDeployment -Name mynewstorageaccount -ResourceGroupName myrg
True

PS C:\> Get-Job 1

Id     Name            PSJobTypeName   State         HasMoreData     Location             Command
--     ----            -------------   -----         -----------     --------             -------
1      Long Running... AzureLongRun... Failed        True            localhost            New-AzResourceGro...
```

## <span data-ttu-id="9274f-120">변수</span><span class="sxs-lookup"><span data-stu-id="9274f-120">PARAMETERS</span></span>

### <span data-ttu-id="9274f-121">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="9274f-121">-ApiVersion</span></span>
<span data-ttu-id="9274f-122">리소스 공급자가 지 원하는 API 버전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9274f-122">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="9274f-123">기본 버전 외의 다른 버전을 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9274f-123">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="9274f-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9274f-124">-DefaultProfile</span></span>
<span data-ttu-id="9274f-125">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="9274f-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9274f-126">-Id</span><span class="sxs-lookup"><span data-stu-id="9274f-126">-Id</span></span>
<span data-ttu-id="9274f-127">중지할 리소스 그룹 배포의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9274f-127">Specifies the ID of the resource group deployment to stop.</span></span>

```yaml
Type: System.String
Parameter Sets: StopByResourceGroupDeploymentId
Aliases: DeploymentId, ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9274f-128">-이름</span><span class="sxs-lookup"><span data-stu-id="9274f-128">-Name</span></span>
<span data-ttu-id="9274f-129">중지할 리소스 그룹 배포의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9274f-129">Specifies the name of the resource group deployment to stop.</span></span>
<span data-ttu-id="9274f-130">이 매개 변수를 지정 하지 않으면이 cmdlet이 리소스 그룹에서 실행 중인 배포를 검색 하 고 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="9274f-130">If you do not specify this parameter, this cmdlet searches for a running deployment in the resource group and stops it.</span></span>
<span data-ttu-id="9274f-131">실행 중인 배포를 두 개 이상 찾으면 명령이 실패 합니다.</span><span class="sxs-lookup"><span data-stu-id="9274f-131">If it finds more than one running deployment, the command fails.</span></span>
<span data-ttu-id="9274f-132">배포 이름을 가져오려면 Get-AzResourceGroupDeployment cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="9274f-132">To get the deployment name, use the Get-AzResourceGroupDeployment cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: StopByResourceGroupDeploymentName
Aliases: DeploymentName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9274f-133">-Pre</span><span class="sxs-lookup"><span data-stu-id="9274f-133">-Pre</span></span>
<span data-ttu-id="9274f-134">이 cmdlet이 사용할 버전을 자동으로 결정 하는 경우 시험판 API 버전을 고려 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="9274f-134">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="9274f-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9274f-135">-ResourceGroupName</span></span>
<span data-ttu-id="9274f-136">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9274f-136">Specifies the name of the resource group.</span></span>
<span data-ttu-id="9274f-137">이 cmdlet은이 매개 변수에서 지정 하는 리소스 그룹의 배포를 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="9274f-137">This cmdlet stops the deployment of the resource group that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: StopByResourceGroupDeploymentName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9274f-138">-확인</span><span class="sxs-lookup"><span data-stu-id="9274f-138">-Confirm</span></span>
<span data-ttu-id="9274f-139">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="9274f-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9274f-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9274f-140">-WhatIf</span></span>
<span data-ttu-id="9274f-141">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="9274f-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9274f-142">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9274f-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9274f-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9274f-143">CommonParameters</span></span>
<span data-ttu-id="9274f-144">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="9274f-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9274f-145">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="9274f-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9274f-146">입력</span><span class="sxs-lookup"><span data-stu-id="9274f-146">INPUTS</span></span>

### <span data-ttu-id="9274f-147">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="9274f-147">System.String</span></span>

## <span data-ttu-id="9274f-148">출력</span><span class="sxs-lookup"><span data-stu-id="9274f-148">OUTPUTS</span></span>

### <span data-ttu-id="9274f-149">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="9274f-149">System.Boolean</span></span>

## <span data-ttu-id="9274f-150">상속자</span><span class="sxs-lookup"><span data-stu-id="9274f-150">NOTES</span></span>

## <span data-ttu-id="9274f-151">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9274f-151">RELATED LINKS</span></span>

[<span data-ttu-id="9274f-152">Get-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="9274f-152">Get-AzResourceGroupDeployment</span></span>](./Get-AzResourceGroupDeployment.md)

[<span data-ttu-id="9274f-153">새로운 AzResource</span><span class="sxs-lookup"><span data-stu-id="9274f-153">New-AzResource</span></span>](./New-AzResource.md)

[<span data-ttu-id="9274f-154">새로운 AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="9274f-154">New-AzResourceGroup</span></span>](./New-AzResourceGroup.md)

[<span data-ttu-id="9274f-155">새로운 AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="9274f-155">New-AzResourceGroupDeployment</span></span>](./New-AzResourceGroupDeployment.md)

[<span data-ttu-id="9274f-156">제거-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="9274f-156">Remove-AzResourceGroupDeployment</span></span>](./Remove-AzResourceGroupDeployment.md)

[<span data-ttu-id="9274f-157">테스트-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="9274f-157">Test-AzResourceGroupDeployment</span></span>](./Test-AzResourceGroupDeployment.md)


