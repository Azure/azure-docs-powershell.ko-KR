---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-aztenantdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzTenantDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzTenantDeployment.md
ms.openlocfilehash: ae9257860a54943dfe262d1574f834404ae0e3ff
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94204397"
---
# <span data-ttu-id="23636-101">Remove-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="23636-101">Remove-AzTenantDeployment</span></span>

## <span data-ttu-id="23636-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="23636-102">SYNOPSIS</span></span>
<span data-ttu-id="23636-103">테 넌 트 범위 및 연결 된 작업에서 배포를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="23636-103">Removes a deployment at tenant scope and any associated operations</span></span>

## <span data-ttu-id="23636-104">구문과</span><span class="sxs-lookup"><span data-stu-id="23636-104">SYNTAX</span></span>

### <span data-ttu-id="23636-105">RemoveByDeploymentName (기본값)</span><span class="sxs-lookup"><span data-stu-id="23636-105">RemoveByDeploymentName (Default)</span></span>
```
Remove-AzTenantDeployment [-Name] <String> [-AsJob] [-PassThru] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="23636-106">RemoveByDeploymentId</span><span class="sxs-lookup"><span data-stu-id="23636-106">RemoveByDeploymentId</span></span>
```
Remove-AzTenantDeployment -Id <String> [-AsJob] [-PassThru] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="23636-107">RemoveByInputObject</span><span class="sxs-lookup"><span data-stu-id="23636-107">RemoveByInputObject</span></span>
```
Remove-AzTenantDeployment -InputObject <PSDeployment> [-AsJob] [-PassThru] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="23636-108">설명은</span><span class="sxs-lookup"><span data-stu-id="23636-108">DESCRIPTION</span></span>
<span data-ttu-id="23636-109">**AzTenantDeployment** cmdlet은 현재 테 넌 트 범위 및 연결 된 작업에서 Azure 배포를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="23636-109">The **Remove-AzTenantDeployment** cmdlet removes an Azure deployment at the current tenant scope and any associated operations.</span></span>

## <span data-ttu-id="23636-110">예제의</span><span class="sxs-lookup"><span data-stu-id="23636-110">EXAMPLES</span></span>

### <span data-ttu-id="23636-111">예제 1: 지정 된 이름을 사용 하 여 배포 제거</span><span class="sxs-lookup"><span data-stu-id="23636-111">Example 1: Remove a deployment with a given name</span></span>
```
PS C:\>Remove-AzTenantDeployment -Name "RolesDeployment"
```

<span data-ttu-id="23636-112">이 명령은 현재 테 넌 트 범위에서 배포 "역할 배포"를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="23636-112">This command removes the deployment "RolesDeployment" at the current tenant scope.</span></span>

### <span data-ttu-id="23636-113">예제 2: 배포 가져오기 및 제거</span><span class="sxs-lookup"><span data-stu-id="23636-113">Example 2: Get a deployment and remove it</span></span>
```
PS C:\>Get-AzTenantDeployment -Name "RolesDeployment" | Remove-AzTenantDeployment
```

<span data-ttu-id="23636-114">이 명령은 현재 테 넌 트 범위의 배포 "역할 배포"를 가져와 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="23636-114">This command gets the deployment "RolesDeployment" at the current tenant scope and removes it.</span></span>

## <span data-ttu-id="23636-115">변수</span><span class="sxs-lookup"><span data-stu-id="23636-115">PARAMETERS</span></span>

### <span data-ttu-id="23636-116">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="23636-116">-ApiVersion</span></span>
<span data-ttu-id="23636-117">설정 되 면 사용할 리소스 공급자 API의 버전을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="23636-117">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="23636-118">지정 하지 않으면 API 버전이 최신 버전으로 자동 결정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="23636-118">If not specified, the API version is automatically determined as the latest available.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23636-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="23636-119">-AsJob</span></span>
<span data-ttu-id="23636-120">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="23636-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="23636-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23636-121">-DefaultProfile</span></span>
<span data-ttu-id="23636-122">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="23636-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23636-123">-Id</span><span class="sxs-lookup"><span data-stu-id="23636-123">-Id</span></span>
<span data-ttu-id="23636-124">배포의 정규화 된 리소스 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="23636-124">The fully qualified resource Id of the deployment.</span></span>
<span data-ttu-id="23636-125">예:/providers/Microsoft.Resources/deployments/{deploymentName}</span><span class="sxs-lookup"><span data-stu-id="23636-125">example: /providers/Microsoft.Resources/deployments/{deploymentName}</span></span>

```yaml
Type: String
Parameter Sets: RemoveByDeploymentId
Aliases: DeploymentId, ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23636-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="23636-126">-InputObject</span></span>
<span data-ttu-id="23636-127">배포 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="23636-127">The deployment object.</span></span>

```yaml
Type: PSDeployment
Parameter Sets: RemoveByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="23636-128">-이름</span><span class="sxs-lookup"><span data-stu-id="23636-128">-Name</span></span>
<span data-ttu-id="23636-129">배포의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="23636-129">The name of the deployment.</span></span>

```yaml
Type: String
Parameter Sets: RemoveByDeploymentName
Aliases: DeploymentName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23636-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="23636-130">-PassThru</span></span>
<span data-ttu-id="23636-131">{{Fill PassThru 설명}}</span><span class="sxs-lookup"><span data-stu-id="23636-131">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="23636-132">-Pre</span><span class="sxs-lookup"><span data-stu-id="23636-132">-Pre</span></span>
<span data-ttu-id="23636-133">설정 하는 경우 cmdlet에서 사용할 버전을 자동으로 결정할 때 시험판 API 버전을 사용 해야 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="23636-133">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="23636-134">-확인</span><span class="sxs-lookup"><span data-stu-id="23636-134">-Confirm</span></span>
<span data-ttu-id="23636-135">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="23636-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="23636-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="23636-136">-WhatIf</span></span>
<span data-ttu-id="23636-137">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="23636-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="23636-138">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="23636-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="23636-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23636-139">CommonParameters</span></span>
<span data-ttu-id="23636-140">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="23636-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23636-141">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="23636-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23636-142">입력</span><span class="sxs-lookup"><span data-stu-id="23636-142">INPUTS</span></span>

### <span data-ttu-id="23636-143">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="23636-143">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="23636-144">출력</span><span class="sxs-lookup"><span data-stu-id="23636-144">OUTPUTS</span></span>

### <span data-ttu-id="23636-145">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="23636-145">System.Boolean</span></span>

## <span data-ttu-id="23636-146">상속자</span><span class="sxs-lookup"><span data-stu-id="23636-146">NOTES</span></span>

## <span data-ttu-id="23636-147">관련 링크</span><span class="sxs-lookup"><span data-stu-id="23636-147">RELATED LINKS</span></span>
