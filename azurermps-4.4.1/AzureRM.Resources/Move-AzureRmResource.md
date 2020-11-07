---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 60BED40A-EEA4-4667-93E9-8A9B35037726
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Move-AzureRmResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Move-AzureRmResource.md
ms.openlocfilehash: 4a40b3fd0045a48d6a69c76970b3835ef2d685c8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93703329"
---
# <span data-ttu-id="93b5a-101">Move-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="93b5a-101">Move-AzureRmResource</span></span>

## <span data-ttu-id="93b5a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="93b5a-102">SYNOPSIS</span></span>
<span data-ttu-id="93b5a-103">리소스를 다른 리소스 그룹 또는 구독으로 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="93b5a-103">Moves a resource to a different resource group or subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="93b5a-104">구문과</span><span class="sxs-lookup"><span data-stu-id="93b5a-104">SYNTAX</span></span>

```
Move-AzureRmResource -DestinationResourceGroupName <String> [-DestinationSubscriptionId <Guid>]
 -ResourceId <String[]> [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="93b5a-105">설명은</span><span class="sxs-lookup"><span data-stu-id="93b5a-105">DESCRIPTION</span></span>
<span data-ttu-id="93b5a-106">**AzureRmResource** cmdlet은 기존 리소스를 다른 리소스 그룹으로 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="93b5a-106">The **Move-AzureRmResource** cmdlet moves existing resources to a different resource group.</span></span>
<span data-ttu-id="93b5a-107">해당 리소스 그룹은 다른 구독에 있을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="93b5a-107">That resource group can be in a different subscription.</span></span>

## <span data-ttu-id="93b5a-108">예제의</span><span class="sxs-lookup"><span data-stu-id="93b5a-108">EXAMPLES</span></span>

### <span data-ttu-id="93b5a-109">예제 1: 리소스 그룹으로 리소스 이동</span><span class="sxs-lookup"><span data-stu-id="93b5a-109">Example 1: Move a resource to a resource group</span></span>
```
PS C:\>$Resource = Get-AzureRmResource -ResourceType "Microsoft.ClassicCompute/storageAccounts" -ResourceName "ContosoStorageAccount"
PS C:\> Move-AzureRmResource -ResourceId $Resource.ResourceId -DestinationResourceGroupName "ResourceGroup14"
```

<span data-ttu-id="93b5a-110">첫 번째 명령은 Get-AzureRmResource cmdlet을 사용 하 여 ContosoStorageAccount 이라는 리소스를 가져온 다음 해당 리소스를 $Resource 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="93b5a-110">The first command gets a resource named ContosoStorageAccount by using the Get-AzureRmResource cmdlet, and then stores that resource in the $Resource variable.</span></span>

<span data-ttu-id="93b5a-111">두 번째 명령은 해당 리소스를 ResourceGroup14 이라는 리소스 그룹으로 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="93b5a-111">The second command moves that resource into the resource group named ResourceGroup14.</span></span>
<span data-ttu-id="93b5a-112">명령은 $Resource의 **ResourceId** 속성을 사용 하 여 이동할 리소스를 식별 합니다.</span><span class="sxs-lookup"><span data-stu-id="93b5a-112">The command identifies the resource to move by using the **ResourceId** property of $Resource.</span></span>

## <span data-ttu-id="93b5a-113">변수</span><span class="sxs-lookup"><span data-stu-id="93b5a-113">PARAMETERS</span></span>

### <span data-ttu-id="93b5a-114">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="93b5a-114">-ApiVersion</span></span>
<span data-ttu-id="93b5a-115">사용할 리소스 공급자 API의 버전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="93b5a-115">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="93b5a-116">버전을 지정 하지 않으면이 cmdlet은 사용 가능한 최신 버전을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="93b5a-116">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="93b5a-117">-DestinationResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="93b5a-117">-DestinationResourceGroupName</span></span>
<span data-ttu-id="93b5a-118">이 cmdlet이 리소스를 이동할 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="93b5a-118">Specifies the name of the resource group into which this cmdlet moves resources.</span></span>

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

### <span data-ttu-id="93b5a-119">-DestinationSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="93b5a-119">-DestinationSubscriptionId</span></span>
<span data-ttu-id="93b5a-120">이 cmdlet이 리소스를 이동할 구독의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="93b5a-120">Specifies the ID of the subscription into which this cmdlet moves resources .</span></span>

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

### <span data-ttu-id="93b5a-121">-Force</span><span class="sxs-lookup"><span data-stu-id="93b5a-121">-Force</span></span>
<span data-ttu-id="93b5a-122">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="93b5a-122">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="93b5a-123">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="93b5a-123">-InformationAction</span></span>
<span data-ttu-id="93b5a-124">이 cmdlet이 정보 이벤트에 응답 하는 방법을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="93b5a-124">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="93b5a-125">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="93b5a-125">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="93b5a-126">하기로</span><span class="sxs-lookup"><span data-stu-id="93b5a-126">Continue</span></span>
- <span data-ttu-id="93b5a-127">숨기기</span><span class="sxs-lookup"><span data-stu-id="93b5a-127">Ignore</span></span>
- <span data-ttu-id="93b5a-128">Inquire</span><span class="sxs-lookup"><span data-stu-id="93b5a-128">Inquire</span></span>
- <span data-ttu-id="93b5a-129">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="93b5a-129">SilentlyContinue</span></span>
- <span data-ttu-id="93b5a-130">중지가</span><span class="sxs-lookup"><span data-stu-id="93b5a-130">Stop</span></span>
- <span data-ttu-id="93b5a-131">대기</span><span class="sxs-lookup"><span data-stu-id="93b5a-131">Suspend</span></span>

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

### <span data-ttu-id="93b5a-132">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="93b5a-132">-InformationVariable</span></span>
<span data-ttu-id="93b5a-133">정보 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="93b5a-133">Specifies an information variable.</span></span>

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

### <span data-ttu-id="93b5a-134">-Pre</span><span class="sxs-lookup"><span data-stu-id="93b5a-134">-Pre</span></span>
<span data-ttu-id="93b5a-135">이 cmdlet이 사용할 버전을 자동으로 결정 하는 경우 시험판 API 버전을 고려 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="93b5a-135">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="93b5a-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="93b5a-136">-ResourceId</span></span>
<span data-ttu-id="93b5a-137">이 cmdlet이 이동 하는 리소스의 Id 배열을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="93b5a-137">Specifies an array of IDs of the resources that this cmdlet moves.</span></span>

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

### <span data-ttu-id="93b5a-138">-확인</span><span class="sxs-lookup"><span data-stu-id="93b5a-138">-Confirm</span></span>
<span data-ttu-id="93b5a-139">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="93b5a-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="93b5a-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="93b5a-140">-WhatIf</span></span>
<span data-ttu-id="93b5a-141">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="93b5a-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="93b5a-142">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="93b5a-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="93b5a-143">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="93b5a-143">-DefaultProfile</span></span>
<span data-ttu-id="93b5a-144">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="93b5a-144">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="93b5a-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93b5a-145">CommonParameters</span></span>
<span data-ttu-id="93b5a-146">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="93b5a-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93b5a-147">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="93b5a-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93b5a-148">입력</span><span class="sxs-lookup"><span data-stu-id="93b5a-148">INPUTS</span></span>

### <span data-ttu-id="93b5a-149">String []</span><span class="sxs-lookup"><span data-stu-id="93b5a-149">String[]</span></span>
<span data-ttu-id="93b5a-150">' ResourceId ' 매개 변수는 파이프라인에서 ' String [] ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="93b5a-150">Parameter 'ResourceId' accepts value of type 'String[]' from the pipeline</span></span>

## <span data-ttu-id="93b5a-151">출력</span><span class="sxs-lookup"><span data-stu-id="93b5a-151">OUTPUTS</span></span>

### <span data-ttu-id="93b5a-152">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="93b5a-152">System.Boolean</span></span>

## <span data-ttu-id="93b5a-153">상속자</span><span class="sxs-lookup"><span data-stu-id="93b5a-153">NOTES</span></span>

## <span data-ttu-id="93b5a-154">관련 링크</span><span class="sxs-lookup"><span data-stu-id="93b5a-154">RELATED LINKS</span></span>

[<span data-ttu-id="93b5a-155">찾기-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="93b5a-155">Find-AzureRmResource</span></span>](./Find-AzureRmResource.md)

[<span data-ttu-id="93b5a-156">Get-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="93b5a-156">Get-AzureRmResource</span></span>](./Get-AzureRmResource.md)

[<span data-ttu-id="93b5a-157">새로운 AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="93b5a-157">New-AzureRmResource</span></span>](./New-AzureRmResource.md)

[<span data-ttu-id="93b5a-158">제거-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="93b5a-158">Remove-AzureRmResource</span></span>](./Remove-AzureRmResource.md)

[<span data-ttu-id="93b5a-159">Set-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="93b5a-159">Set-AzureRmResource</span></span>](./Set-AzureRmResource.md)


