---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 880D321E-30F2-4CAE-B14A-5F6DD8E1DB99
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmResourceGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmResourceGroup.md
ms.openlocfilehash: 6938cf80f3fa6fb20252e1e4a212133ecd1c62a9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93532947"
---
# <span data-ttu-id="d0035-101">Remove-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="d0035-101">Remove-AzureRmResourceGroup</span></span>

## <span data-ttu-id="d0035-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d0035-102">SYNOPSIS</span></span>
<span data-ttu-id="d0035-103">리소스 그룹을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="d0035-103">Removes a resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d0035-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d0035-104">SYNTAX</span></span>

### <span data-ttu-id="d0035-105">이름에 따라 리소스 그룹을 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="d0035-105">Lists the resource group based in the name.</span></span> <span data-ttu-id="d0035-106">기본값</span><span class="sxs-lookup"><span data-stu-id="d0035-106">(Default)</span></span>
```
Remove-AzureRmResourceGroup [-Name] <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d0035-107">Id를 기준으로 리소스 그룹을 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="d0035-107">Lists the resource group based in the Id.</span></span>
```
Remove-AzureRmResourceGroup [-Id] <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d0035-108">설명은</span><span class="sxs-lookup"><span data-stu-id="d0035-108">DESCRIPTION</span></span>
<span data-ttu-id="d0035-109">**AzureRmResourceGroup** cmdlet은 현재 구독에서 Azure 리소스 그룹과 해당 리소스를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="d0035-109">The **Remove-AzureRmResourceGroup** cmdlet removes an Azure resource group and its resources from the current subscription.</span></span>
<span data-ttu-id="d0035-110">리소스를 삭제 하 되 리소스 그룹을 유지 하려면 Remove-AzureRmResource cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="d0035-110">To delete a resource, but leave the resource group, use the Remove-AzureRmResource cmdlet.</span></span>

## <span data-ttu-id="d0035-111">예제의</span><span class="sxs-lookup"><span data-stu-id="d0035-111">EXAMPLES</span></span>

### <span data-ttu-id="d0035-112">예제 1: 리소스 그룹 제거</span><span class="sxs-lookup"><span data-stu-id="d0035-112">Example 1: Remove a resource group</span></span>
```
PS C:\>Remove-AzureRmResourceGroup -Name "ContosoRG01"
```

<span data-ttu-id="d0035-113">이 명령은 구독에서 ContosoRG01 리소스 그룹을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="d0035-113">This command removes the ContosoRG01 resource group from the subscription.</span></span>
<span data-ttu-id="d0035-114">Cmdlet에서 확인을 요청 하 고 출력을 반환 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d0035-114">The cmdlet prompts you for confirmation and returns no output.</span></span>

### <span data-ttu-id="d0035-115">예제 2: 확인 하지 않고 리소스 그룹 제거</span><span class="sxs-lookup"><span data-stu-id="d0035-115">Example 2: Remove a resource group without confirmation</span></span>
```
PS C:\>Get-AzureRmResourceGroup -Name "ContosoRG01" | Remove-AzureRmResourceGroup -Verbose -Force
```

<span data-ttu-id="d0035-116">이 명령은 Get-AzureRmResourceGroup cmdlet을 사용 하 여 리소스 그룹 ContosoRG01을 얻은 다음 pipeline 연산자를 사용 하 여 **Remove-AzureRmResourceGroup** 에 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="d0035-116">This command uses the Get-AzureRmResourceGroup cmdlet to get the resource group ContosoRG01, and then passes it to **Remove-AzureRmResourceGroup** by using the pipeline operator.</span></span>
<span data-ttu-id="d0035-117">*Verbose* 공용 매개 변수는 연산에 대 한 상태 정보를 가져오며 *Force* 매개 변수는 확인 메시지를 표시 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d0035-117">The *Verbose* common parameter gets status information about the operation, and the *Force* parameter suppresses the confirmation prompt.</span></span>

### <span data-ttu-id="d0035-118">예제 3: 모든 리소스 그룹 제거</span><span class="sxs-lookup"><span data-stu-id="d0035-118">Example 3: Remove all resource groups</span></span>
```
PS C:\>Get-AzureRmResourceGroup | Remove-AzureRmResourceGroup
```

<span data-ttu-id="d0035-119">이 명령은 **AzureRmResourceGroup** cmdlet을 사용 하 여 모든 리소스 그룹을 가져와 해당 파이프라인 연산자를 사용 하 여 **Remove-AzureRmResourceGroup** 에 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="d0035-119">This command uses the **Get-AzureRmResourceGroup** cmdlet to get all resource groups, and then passes them to **Remove-AzureRmResourceGroup** by using the pipeline operator.</span></span>

## <span data-ttu-id="d0035-120">변수</span><span class="sxs-lookup"><span data-stu-id="d0035-120">PARAMETERS</span></span>

### <span data-ttu-id="d0035-121">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="d0035-121">-ApiVersion</span></span>
<span data-ttu-id="d0035-122">리소스 공급자가 지 원하는 API 버전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d0035-122">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="d0035-123">기본 버전 외의 다른 버전을 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d0035-123">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="d0035-124">-Force</span><span class="sxs-lookup"><span data-stu-id="d0035-124">-Force</span></span>
<span data-ttu-id="d0035-125">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="d0035-125">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="d0035-126">-Id</span><span class="sxs-lookup"><span data-stu-id="d0035-126">-Id</span></span>
<span data-ttu-id="d0035-127">제거할 리소스 그룹의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d0035-127">Specifies the ID of resource group to remove.</span></span>
<span data-ttu-id="d0035-128">와일드 카드 문자는 허용 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d0035-128">Wildcard characters are not permitted.</span></span>

```yaml
Type: System.String
Parameter Sets: Lists the resource group based in the Id.
Aliases: ResourceGroupId, ResourceId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d0035-129">-이름</span><span class="sxs-lookup"><span data-stu-id="d0035-129">-Name</span></span>
<span data-ttu-id="d0035-130">제거할 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d0035-130">Specifies the names of resource groups to remove.</span></span>
<span data-ttu-id="d0035-131">와일드 카드 문자는 허용 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d0035-131">Wildcard characters are not permitted.</span></span>

```yaml
Type: System.String
Parameter Sets: Lists the resource group based in the name.
Aliases: ResourceGroupName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d0035-132">-Pre</span><span class="sxs-lookup"><span data-stu-id="d0035-132">-Pre</span></span>
<span data-ttu-id="d0035-133">이 cmdlet이 사용할 버전을 자동으로 결정 하는 경우 시험판 API 버전을 고려 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="d0035-133">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="d0035-134">-확인</span><span class="sxs-lookup"><span data-stu-id="d0035-134">-Confirm</span></span>
<span data-ttu-id="d0035-135">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="d0035-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d0035-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d0035-136">-WhatIf</span></span>
<span data-ttu-id="d0035-137">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="d0035-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d0035-138">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d0035-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d0035-139">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d0035-139">-DefaultProfile</span></span>
<span data-ttu-id="d0035-140">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d0035-140">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d0035-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d0035-141">CommonParameters</span></span>
<span data-ttu-id="d0035-142">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d0035-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d0035-143">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d0035-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d0035-144">입력</span><span class="sxs-lookup"><span data-stu-id="d0035-144">INPUTS</span></span>

### <span data-ttu-id="d0035-145">않아야</span><span class="sxs-lookup"><span data-stu-id="d0035-145">None</span></span>

## <span data-ttu-id="d0035-146">출력</span><span class="sxs-lookup"><span data-stu-id="d0035-146">OUTPUTS</span></span>

### <span data-ttu-id="d0035-147">않아야</span><span class="sxs-lookup"><span data-stu-id="d0035-147">None</span></span>

## <span data-ttu-id="d0035-148">상속자</span><span class="sxs-lookup"><span data-stu-id="d0035-148">NOTES</span></span>

## <span data-ttu-id="d0035-149">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d0035-149">RELATED LINKS</span></span>

[<span data-ttu-id="d0035-150">Get-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="d0035-150">Get-AzureRmResourceGroup</span></span>](./Get-AzureRmResourceGroup.md)

[<span data-ttu-id="d0035-151">새로운 AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="d0035-151">New-AzureRmResourceGroup</span></span>](./New-AzureRmResourceGroup.md)

[<span data-ttu-id="d0035-152">Set-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="d0035-152">Set-AzureRmResourceGroup</span></span>](./Set-AzureRmResourceGroup.md)


