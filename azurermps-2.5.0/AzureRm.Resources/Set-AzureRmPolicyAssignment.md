---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: C3B2C33F-8BD4-4E31-9450-EF6A3A6A5325
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/set-azurermpolicyassignment
schema: 2.0.0
ms.openlocfilehash: dc54d84886bc9c13fa6a4ecef4e41ef80fa6d4e4
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93881273"
---
# <span data-ttu-id="b369b-101">Set-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="b369b-101">Set-AzureRmPolicyAssignment</span></span>

## <span data-ttu-id="b369b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b369b-102">SYNOPSIS</span></span>
<span data-ttu-id="b369b-103">정책 할당을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b369b-103">Modifies a policy assignment.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b369b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b369b-104">SYNTAX</span></span>

### <span data-ttu-id="b369b-105">NameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="b369b-105">NameParameterSet (Default)</span></span>
```
Set-AzureRmPolicyAssignment -Name <String> -Scope <String> [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-Metadata <String>] [-Sku <Hashtable>] [-AssignIdentity] [-Location <String>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="b369b-106">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b369b-106">IdParameterSet</span></span>
```
Set-AzureRmPolicyAssignment [-NotScope <String[]>] -Id <String> [-DisplayName <String>] [-Description <String>]
 [-Metadata <String>] [-Sku <Hashtable>] [-AssignIdentity] [-Location <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="b369b-107">설명은</span><span class="sxs-lookup"><span data-stu-id="b369b-107">DESCRIPTION</span></span>
<span data-ttu-id="b369b-108">**Set-AzureRmPolicyAssignment** cmdlet은 정책 할당을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b369b-108">The **Set-AzureRmPolicyAssignment** cmdlet modifies a policy assignment.</span></span>
<span data-ttu-id="b369b-109">ID 또는 이름 및 범위를 기준으로 과제를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b369b-109">Specify an assignment by ID or by name and scope.</span></span>

## <span data-ttu-id="b369b-110">예제의</span><span class="sxs-lookup"><span data-stu-id="b369b-110">EXAMPLES</span></span>

### <span data-ttu-id="b369b-111">예제 1: 표시 이름 업데이트</span><span class="sxs-lookup"><span data-stu-id="b369b-111">Example 1: Update the display name</span></span>
```
PS C:\> $ResourceGroup = Get-AzureRmResourceGroup -Name 'ResourceGroup11'
PS C:\> $PolicyAssignment = Get-AzureRmPolicyAssignment -Name 'PolicyAssignment' -Scope $ResourceGroup.ResourceId
PS C:\> Set-AzureRmPolicyAssignment -Id $PolicyAssignment.ResourceId -DisplayName 'Do not allow VM creation'
```

<span data-ttu-id="b369b-112">첫 번째 명령은 Get-AzureRMResourceGroup cmdlet을 사용 하 여 ResourceGroup11 이라는 리소스 그룹을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b369b-112">The first command gets a resource group named ResourceGroup11 by using the Get-AzureRMResourceGroup cmdlet.</span></span>
<span data-ttu-id="b369b-113">명령이 $ResourceGroup 변수에 해당 개체를 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="b369b-113">The command stores that object in the $ResourceGroup variable.</span></span>
<span data-ttu-id="b369b-114">두 번째 명령은 Get-AzureRmPolicyAssignment cmdlet을 사용 하 여 PolicyAssignment 이라는 정책 과제를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b369b-114">The second command gets the policy assignment named PolicyAssignment by using the Get-AzureRmPolicyAssignment cmdlet.</span></span>
<span data-ttu-id="b369b-115">명령이 $PolicyAssignment 변수에 해당 개체를 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="b369b-115">The command stores that object in the $PolicyAssignment variable.</span></span>
<span data-ttu-id="b369b-116">마지막 명령은 $ResourceGroup의 **ResourceId** 속성으로 식별 되는 리소스 그룹의 정책 할당에 대 한 표시 이름을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="b369b-116">The final command updates the display name on the policy assignment on the resource group identified by the **ResourceId** property of $ResourceGroup.</span></span>

### <span data-ttu-id="b369b-117">예제 2: 정책 할당에 관리 되는 id 추가</span><span class="sxs-lookup"><span data-stu-id="b369b-117">Example 2: Add a managed identity to the policy assignment</span></span>
```
PS C:\> $PolicyAssignment = Get-AzureRmPolicyAssignment -Name 'PolicyAssignment'
PS C:\> Set-AzureRmPolicyAssignment -Id $PolicyAssignment.ResourceId -AssignIdentity -Location 'westus'
```

<span data-ttu-id="b369b-118">첫 번째 명령은 Get-AzureRmPolicyAssignment cmdlet을 사용 하 여 현재 구독에서 PolicyAssignment 이라는 정책 과제를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b369b-118">The first command gets the policy assignment named PolicyAssignment from the current subscription by using the Get-AzureRmPolicyAssignment cmdlet.</span></span>
<span data-ttu-id="b369b-119">명령이 $PolicyAssignment 변수에 해당 개체를 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="b369b-119">The command stores that object in the $PolicyAssignment variable.</span></span>
<span data-ttu-id="b369b-120">마지막 명령은 정책 할당에 관리 되는 id를 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="b369b-120">The final command assigns a managed identity to the policy assignment.</span></span>

## <span data-ttu-id="b369b-121">변수</span><span class="sxs-lookup"><span data-stu-id="b369b-121">PARAMETERS</span></span>

### <span data-ttu-id="b369b-122">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="b369b-122">-ApiVersion</span></span>
<span data-ttu-id="b369b-123">사용할 리소스 공급자 API의 버전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b369b-123">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="b369b-124">버전을 지정 하지 않으면이 cmdlet은 사용 가능한 최신 버전을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="b369b-124">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="b369b-125">-Id 할당</span><span class="sxs-lookup"><span data-stu-id="b369b-125">-AssignIdentity</span></span>
<span data-ttu-id="b369b-126">이 정책 할당에 대 한 Azure Active Directory Id를 생성 하 고 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="b369b-126">Generate and assign an Azure Active Directory Identity for this policy assignment.</span></span> <span data-ttu-id="b369b-127">Id는 ' deployIfNotExists ' 정책에 대 한 배포를 실행 하는 경우에 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b369b-127">The identity will be used when executing deployments for 'deployIfNotExists' policies.</span></span> <span data-ttu-id="b369b-128">Id를 할당할 때 위치가 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="b369b-128">Location is required when assigning an identity.</span></span>

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

### <span data-ttu-id="b369b-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b369b-129">-DefaultProfile</span></span>
<span data-ttu-id="b369b-130">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="b369b-130">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b369b-131">-설명</span><span class="sxs-lookup"><span data-stu-id="b369b-131">-Description</span></span>
<span data-ttu-id="b369b-132">정책 할당에 대 한 설명</span><span class="sxs-lookup"><span data-stu-id="b369b-132">The description for policy assignment</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b369b-133">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="b369b-133">-DisplayName</span></span>
<span data-ttu-id="b369b-134">정책 할당에 대 한 새 표시 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b369b-134">Specifies a new display name for the policy assignment.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b369b-135">-Id</span><span class="sxs-lookup"><span data-stu-id="b369b-135">-Id</span></span>
<span data-ttu-id="b369b-136">이 cmdlet이 수정 하는 정책 할당에 대 한 정규화 된 리소스 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b369b-136">Specifies the fully qualified resource ID for the policy assignment that this cmdlet modifies.</span></span>

```yaml
Type: System.String
Parameter Sets: IdParameterSet
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b369b-137">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="b369b-137">-InformationAction</span></span>
<span data-ttu-id="b369b-138">이 cmdlet이 정보 이벤트에 응답 하는 방법을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b369b-138">Specifies how this cmdlet responds to an information event.</span></span>
<span data-ttu-id="b369b-139">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="b369b-139">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="b369b-140">하기로</span><span class="sxs-lookup"><span data-stu-id="b369b-140">Continue</span></span>
- <span data-ttu-id="b369b-141">숨기기</span><span class="sxs-lookup"><span data-stu-id="b369b-141">Ignore</span></span>
- <span data-ttu-id="b369b-142">Inquire</span><span class="sxs-lookup"><span data-stu-id="b369b-142">Inquire</span></span>
- <span data-ttu-id="b369b-143">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="b369b-143">SilentlyContinue</span></span>
- <span data-ttu-id="b369b-144">중지가</span><span class="sxs-lookup"><span data-stu-id="b369b-144">Stop</span></span>
- <span data-ttu-id="b369b-145">대기</span><span class="sxs-lookup"><span data-stu-id="b369b-145">Suspend</span></span>

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

### <span data-ttu-id="b369b-146">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="b369b-146">-InformationVariable</span></span>
<span data-ttu-id="b369b-147">정보 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b369b-147">Specifies an information variable.</span></span>

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

### <span data-ttu-id="b369b-148">-위치</span><span class="sxs-lookup"><span data-stu-id="b369b-148">-Location</span></span>
<span data-ttu-id="b369b-149">정책 할당의 리소스 id 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="b369b-149">The location of the policy assignment's resource identity.</span></span> <span data-ttu-id="b369b-150">이는-할당 Id 스위치를 사용 하는 경우에 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="b369b-150">This is required when the -AssignIdentity switch is used.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b369b-151">-Metadata</span><span class="sxs-lookup"><span data-stu-id="b369b-151">-Metadata</span></span>
<span data-ttu-id="b369b-152">정책 할당에 대 한 업데이트 된 메타 데이터입니다.</span><span class="sxs-lookup"><span data-stu-id="b369b-152">The updated metadata for the policy assignment.</span></span> <span data-ttu-id="b369b-153">메타 데이터를 포함 하는 파일 이름의 경로 이거나 메타 데이터를 문자열로 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b369b-153">This can either be a path to a file name containing the metadata, or the metadata as a string.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b369b-154">-이름</span><span class="sxs-lookup"><span data-stu-id="b369b-154">-Name</span></span>
<span data-ttu-id="b369b-155">이 cmdlet이 수정 하는 정책 할당의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b369b-155">Specifies the name of the policy assignment that this cmdlet modifies.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b369b-156">-NotScope</span><span class="sxs-lookup"><span data-stu-id="b369b-156">-NotScope</span></span>
<span data-ttu-id="b369b-157">정책 할당이 범위를 지정 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b369b-157">The policy assignment not scopes.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b369b-158">-Pre</span><span class="sxs-lookup"><span data-stu-id="b369b-158">-Pre</span></span>
<span data-ttu-id="b369b-159">이 cmdlet이 사용할 버전을 자동으로 결정 하는 경우 시험판 API 버전을 고려 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="b369b-159">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="b369b-160">-범위</span><span class="sxs-lookup"><span data-stu-id="b369b-160">-Scope</span></span>
<span data-ttu-id="b369b-161">정책이 적용 되는 범위를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b369b-161">Specifies the scope at which the policy is applied.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b369b-162">-Sku</span><span class="sxs-lookup"><span data-stu-id="b369b-162">-Sku</span></span>
<span data-ttu-id="b369b-163">Sku 속성을 나타내는 해시 테이블입니다.</span><span class="sxs-lookup"><span data-stu-id="b369b-163">A hash table which represents sku properties.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: SkuObject

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b369b-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b369b-164">CommonParameters</span></span>
<span data-ttu-id="b369b-165">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b369b-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b369b-166">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b369b-166">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b369b-167">입력</span><span class="sxs-lookup"><span data-stu-id="b369b-167">INPUTS</span></span>

## <span data-ttu-id="b369b-168">출력</span><span class="sxs-lookup"><span data-stu-id="b369b-168">OUTPUTS</span></span>

## <span data-ttu-id="b369b-169">상속자</span><span class="sxs-lookup"><span data-stu-id="b369b-169">NOTES</span></span>

## <span data-ttu-id="b369b-170">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b369b-170">RELATED LINKS</span></span>

[<span data-ttu-id="b369b-171">Get-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="b369b-171">Get-AzureRmPolicyAssignment</span></span>](./Get-AzureRmPolicyAssignment.md)

[<span data-ttu-id="b369b-172">새로운 AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="b369b-172">New-AzureRmPolicyAssignment</span></span>](./New-AzureRmPolicyAssignment.md)

[<span data-ttu-id="b369b-173">제거-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="b369b-173">Remove-AzureRmPolicyAssignment</span></span>](./Remove-AzureRmPolicyAssignment.md)


