---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 60BED40A-EEA4-4667-93E9-8A9B35037726
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/move-azurermresource
schema: 2.0.0
ms.openlocfilehash: 4f50aea600fe930de62a65d566b6a6ec723fc8de
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93882137"
---
# <span data-ttu-id="ed209-101">Move-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="ed209-101">Move-AzureRmResource</span></span>

## <span data-ttu-id="ed209-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ed209-102">SYNOPSIS</span></span>
<span data-ttu-id="ed209-103">리소스를 다른 리소스 그룹 또는 구독으로 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="ed209-103">Moves a resource to a different resource group or subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ed209-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ed209-104">SYNTAX</span></span>

```
Move-AzureRmResource -DestinationResourceGroupName <String> [-DestinationSubscriptionId <Guid>]
 -ResourceId <String[]> [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ed209-105">설명은</span><span class="sxs-lookup"><span data-stu-id="ed209-105">DESCRIPTION</span></span>
<span data-ttu-id="ed209-106">**AzureRmResource** cmdlet은 기존 리소스를 다른 리소스 그룹으로 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="ed209-106">The **Move-AzureRmResource** cmdlet moves existing resources to a different resource group.</span></span>
<span data-ttu-id="ed209-107">해당 리소스 그룹은 다른 구독에 있을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ed209-107">That resource group can be in a different subscription.</span></span>

## <span data-ttu-id="ed209-108">예제의</span><span class="sxs-lookup"><span data-stu-id="ed209-108">EXAMPLES</span></span>

### <span data-ttu-id="ed209-109">예제 1: 리소스 그룹으로 리소스 이동</span><span class="sxs-lookup"><span data-stu-id="ed209-109">Example 1: Move a resource to a resource group</span></span>
```
PS C:\>$Resource = Get-AzureRmResource -ResourceType "Microsoft.ClassicCompute/storageAccounts" -ResourceName "ContosoStorageAccount"
PS C:\> Move-AzureRmResource -ResourceId $Resource.ResourceId -DestinationResourceGroupName "ResourceGroup14"
```

<span data-ttu-id="ed209-110">첫 번째 명령은 Get-AzureRmResource cmdlet을 사용 하 여 ContosoStorageAccount 이라는 리소스를 가져온 다음 해당 리소스를 $Resource 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="ed209-110">The first command gets a resource named ContosoStorageAccount by using the Get-AzureRmResource cmdlet, and then stores that resource in the $Resource variable.</span></span>
<span data-ttu-id="ed209-111">두 번째 명령은 해당 리소스를 ResourceGroup14 이라는 리소스 그룹으로 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="ed209-111">The second command moves that resource into the resource group named ResourceGroup14.</span></span>
<span data-ttu-id="ed209-112">명령은 $Resource의 **ResourceId** 속성을 사용 하 여 이동할 리소스를 식별 합니다.</span><span class="sxs-lookup"><span data-stu-id="ed209-112">The command identifies the resource to move by using the **ResourceId** property of $Resource.</span></span>

## <span data-ttu-id="ed209-113">변수</span><span class="sxs-lookup"><span data-stu-id="ed209-113">PARAMETERS</span></span>

### <span data-ttu-id="ed209-114">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="ed209-114">-ApiVersion</span></span>
<span data-ttu-id="ed209-115">사용할 리소스 공급자 API의 버전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ed209-115">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="ed209-116">버전을 지정 하지 않으면이 cmdlet은 사용 가능한 최신 버전을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="ed209-116">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="ed209-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed209-117">-DefaultProfile</span></span>
<span data-ttu-id="ed209-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="ed209-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ed209-119">-DestinationResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ed209-119">-DestinationResourceGroupName</span></span>
<span data-ttu-id="ed209-120">이 cmdlet이 리소스를 이동할 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ed209-120">Specifies the name of the resource group into which this cmdlet moves resources.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: TargetResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed209-121">-DestinationSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ed209-121">-DestinationSubscriptionId</span></span>
<span data-ttu-id="ed209-122">이 cmdlet이 리소스를 이동할 구독의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ed209-122">Specifies the ID of the subscription into which this cmdlet moves resources .</span></span>

```yaml
Type: System.Nullable`1[System.Guid]
Parameter Sets: (All)
Aliases: Id, SubscriptionId

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed209-123">-Force</span><span class="sxs-lookup"><span data-stu-id="ed209-123">-Force</span></span>
<span data-ttu-id="ed209-124">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="ed209-124">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="ed209-125">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="ed209-125">-InformationAction</span></span>
<span data-ttu-id="ed209-126">이 cmdlet이 정보 이벤트에 응답 하는 방법을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ed209-126">Specifies how this cmdlet responds to an information event.</span></span>
<span data-ttu-id="ed209-127">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="ed209-127">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="ed209-128">하기로</span><span class="sxs-lookup"><span data-stu-id="ed209-128">Continue</span></span>
- <span data-ttu-id="ed209-129">숨기기</span><span class="sxs-lookup"><span data-stu-id="ed209-129">Ignore</span></span>
- <span data-ttu-id="ed209-130">Inquire</span><span class="sxs-lookup"><span data-stu-id="ed209-130">Inquire</span></span>
- <span data-ttu-id="ed209-131">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="ed209-131">SilentlyContinue</span></span>
- <span data-ttu-id="ed209-132">중지가</span><span class="sxs-lookup"><span data-stu-id="ed209-132">Stop</span></span>
- <span data-ttu-id="ed209-133">대기</span><span class="sxs-lookup"><span data-stu-id="ed209-133">Suspend</span></span>

```yaml
Type: System.Management.Automation.ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed209-134">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="ed209-134">-InformationVariable</span></span>
<span data-ttu-id="ed209-135">정보 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ed209-135">Specifies an information variable.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed209-136">-Pre</span><span class="sxs-lookup"><span data-stu-id="ed209-136">-Pre</span></span>
<span data-ttu-id="ed209-137">이 cmdlet이 사용할 버전을 자동으로 결정 하는 경우 시험판 API 버전을 고려 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="ed209-137">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="ed209-138">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ed209-138">-ResourceId</span></span>
<span data-ttu-id="ed209-139">이 cmdlet이 이동 하는 리소스의 Id 배열을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ed209-139">Specifies an array of IDs of the resources that this cmdlet moves.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ed209-140">-확인</span><span class="sxs-lookup"><span data-stu-id="ed209-140">-Confirm</span></span>
<span data-ttu-id="ed209-141">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="ed209-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ed209-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ed209-142">-WhatIf</span></span>
<span data-ttu-id="ed209-143">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="ed209-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ed209-144">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ed209-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ed209-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed209-145">CommonParameters</span></span>
<span data-ttu-id="ed209-146">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ed209-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed209-147">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ed209-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed209-148">입력</span><span class="sxs-lookup"><span data-stu-id="ed209-148">INPUTS</span></span>

## <span data-ttu-id="ed209-149">출력</span><span class="sxs-lookup"><span data-stu-id="ed209-149">OUTPUTS</span></span>

## <span data-ttu-id="ed209-150">상속자</span><span class="sxs-lookup"><span data-stu-id="ed209-150">NOTES</span></span>

## <span data-ttu-id="ed209-151">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ed209-151">RELATED LINKS</span></span>



[<span data-ttu-id="ed209-152">Get-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="ed209-152">Get-AzureRmResource</span></span>](./Get-AzureRmResource.md)

[<span data-ttu-id="ed209-153">새로운 AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="ed209-153">New-AzureRmResource</span></span>](./New-AzureRmResource.md)

[<span data-ttu-id="ed209-154">제거-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="ed209-154">Remove-AzureRmResource</span></span>](./Remove-AzureRmResource.md)

[<span data-ttu-id="ed209-155">Set-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="ed209-155">Set-AzureRmResource</span></span>](./Set-AzureRmResource.md)


