---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: C3B2C33F-8BD4-4E31-9450-EF6A3A6A5325
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/set-azpolicyassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzPolicyAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzPolicyAssignment.md
ms.openlocfilehash: 2b699219281d64e50694f7e7dd70a965626f7132
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93699316"
---
# <span data-ttu-id="f286a-101">Set-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="f286a-101">Set-AzPolicyAssignment</span></span>

## <span data-ttu-id="f286a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f286a-102">SYNOPSIS</span></span>
<span data-ttu-id="f286a-103">정책 할당을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f286a-103">Modifies a policy assignment.</span></span>

## <span data-ttu-id="f286a-104">구문과</span><span class="sxs-lookup"><span data-stu-id="f286a-104">SYNTAX</span></span>

### <span data-ttu-id="f286a-105">NameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="f286a-105">NameParameterSet (Default)</span></span>
```
Set-AzPolicyAssignment -Name <String> -Scope <String> [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-Metadata <String>] [-AssignIdentity] [-Location <String>] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f286a-106">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f286a-106">IdParameterSet</span></span>
```
Set-AzPolicyAssignment [-NotScope <String[]>] -Id <String> [-DisplayName <String>] [-Description <String>]
 [-Metadata <String>] [-AssignIdentity] [-Location <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f286a-107">설명은</span><span class="sxs-lookup"><span data-stu-id="f286a-107">DESCRIPTION</span></span>
<span data-ttu-id="f286a-108">**Set-AzPolicyAssignment** cmdlet은 정책 할당을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f286a-108">The **Set-AzPolicyAssignment** cmdlet modifies a policy assignment.</span></span>
<span data-ttu-id="f286a-109">ID 또는 이름 및 범위를 기준으로 과제를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f286a-109">Specify an assignment by ID or by name and scope.</span></span>

## <span data-ttu-id="f286a-110">예제의</span><span class="sxs-lookup"><span data-stu-id="f286a-110">EXAMPLES</span></span>

### <span data-ttu-id="f286a-111">예제 1: 표시 이름 업데이트</span><span class="sxs-lookup"><span data-stu-id="f286a-111">Example 1: Update the display name</span></span>
```
PS C:\> $ResourceGroup = Get-AzResourceGroup -Name 'ResourceGroup11'
PS C:\> $PolicyAssignment = Get-AzPolicyAssignment -Name 'PolicyAssignment' -Scope $ResourceGroup.ResourceId
PS C:\> Set-AzPolicyAssignment -Id $PolicyAssignment.ResourceId -DisplayName 'Do not allow VM creation'
```

<span data-ttu-id="f286a-112">첫 번째 명령은 Get-AzResourceGroup cmdlet을 사용 하 여 ResourceGroup11 이라는 리소스 그룹을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f286a-112">The first command gets a resource group named ResourceGroup11 by using the Get-AzResourceGroup cmdlet.</span></span>
<span data-ttu-id="f286a-113">명령이 $ResourceGroup 변수에 해당 개체를 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="f286a-113">The command stores that object in the $ResourceGroup variable.</span></span>
<span data-ttu-id="f286a-114">두 번째 명령은 Get-AzPolicyAssignment cmdlet을 사용 하 여 PolicyAssignment 이라는 정책 과제를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f286a-114">The second command gets the policy assignment named PolicyAssignment by using the Get-AzPolicyAssignment cmdlet.</span></span>
<span data-ttu-id="f286a-115">명령이 $PolicyAssignment 변수에 해당 개체를 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="f286a-115">The command stores that object in the $PolicyAssignment variable.</span></span>
<span data-ttu-id="f286a-116">마지막 명령은 $ResourceGroup의 **ResourceId** 속성으로 식별 되는 리소스 그룹의 정책 할당에 대 한 표시 이름을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="f286a-116">The final command updates the display name on the policy assignment on the resource group identified by the **ResourceId** property of $ResourceGroup.</span></span>

### <span data-ttu-id="f286a-117">예제 2: 정책 할당에 관리 되는 id 추가</span><span class="sxs-lookup"><span data-stu-id="f286a-117">Example 2: Add a managed identity to the policy assignment</span></span>
```
PS C:\> $PolicyAssignment = Get-AzPolicyAssignment -Name 'PolicyAssignment'
PS C:\> Set-AzPolicyAssignment -Id $PolicyAssignment.ResourceId -AssignIdentity -Location 'westus'
```

<span data-ttu-id="f286a-118">첫 번째 명령은 Get-AzPolicyAssignment cmdlet을 사용 하 여 현재 구독에서 PolicyAssignment 이라는 정책 과제를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f286a-118">The first command gets the policy assignment named PolicyAssignment from the current subscription by using the Get-AzPolicyAssignment cmdlet.</span></span>
<span data-ttu-id="f286a-119">명령이 $PolicyAssignment 변수에 해당 개체를 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="f286a-119">The command stores that object in the $PolicyAssignment variable.</span></span>
<span data-ttu-id="f286a-120">마지막 명령은 정책 할당에 관리 되는 id를 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="f286a-120">The final command assigns a managed identity to the policy assignment.</span></span>

## <span data-ttu-id="f286a-121">변수</span><span class="sxs-lookup"><span data-stu-id="f286a-121">PARAMETERS</span></span>

### <span data-ttu-id="f286a-122">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="f286a-122">-ApiVersion</span></span>
<span data-ttu-id="f286a-123">사용할 리소스 공급자 API의 버전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f286a-123">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="f286a-124">버전을 지정 하지 않으면이 cmdlet은 사용 가능한 최신 버전을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="f286a-124">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="f286a-125">-Id 할당</span><span class="sxs-lookup"><span data-stu-id="f286a-125">-AssignIdentity</span></span>
<span data-ttu-id="f286a-126">이 정책 할당에 대 한 Azure Active Directory Id를 생성 하 고 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="f286a-126">Generate and assign an Azure Active Directory Identity for this policy assignment.</span></span> <span data-ttu-id="f286a-127">Id는 ' deployIfNotExists ' 정책에 대 한 배포를 실행 하는 경우에 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="f286a-127">The identity will be used when executing deployments for 'deployIfNotExists' policies.</span></span> <span data-ttu-id="f286a-128">Id를 할당할 때 위치가 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="f286a-128">Location is required when assigning an identity.</span></span>

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

### <span data-ttu-id="f286a-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f286a-129">-DefaultProfile</span></span>
<span data-ttu-id="f286a-130">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="f286a-130">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f286a-131">-설명</span><span class="sxs-lookup"><span data-stu-id="f286a-131">-Description</span></span>
<span data-ttu-id="f286a-132">정책 할당에 대 한 설명</span><span class="sxs-lookup"><span data-stu-id="f286a-132">The description for policy assignment</span></span>

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

### <span data-ttu-id="f286a-133">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="f286a-133">-DisplayName</span></span>
<span data-ttu-id="f286a-134">정책 할당에 대 한 새 표시 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f286a-134">Specifies a new display name for the policy assignment.</span></span>

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

### <span data-ttu-id="f286a-135">-Id</span><span class="sxs-lookup"><span data-stu-id="f286a-135">-Id</span></span>
<span data-ttu-id="f286a-136">이 cmdlet이 수정 하는 정책 할당에 대 한 정규화 된 리소스 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f286a-136">Specifies the fully qualified resource ID for the policy assignment that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="f286a-137">-위치</span><span class="sxs-lookup"><span data-stu-id="f286a-137">-Location</span></span>
<span data-ttu-id="f286a-138">정책 할당의 리소스 id 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="f286a-138">The location of the policy assignment's resource identity.</span></span> <span data-ttu-id="f286a-139">이는-할당 Id 스위치를 사용 하는 경우에 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="f286a-139">This is required when the -AssignIdentity switch is used.</span></span>

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

### <span data-ttu-id="f286a-140">-Metadata</span><span class="sxs-lookup"><span data-stu-id="f286a-140">-Metadata</span></span>
<span data-ttu-id="f286a-141">정책 할당에 대 한 업데이트 된 메타 데이터입니다.</span><span class="sxs-lookup"><span data-stu-id="f286a-141">The updated metadata for the policy assignment.</span></span> <span data-ttu-id="f286a-142">메타 데이터를 포함 하는 파일 이름의 경로 이거나 메타 데이터를 문자열로 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f286a-142">This can either be a path to a file name containing the metadata, or the metadata as a string.</span></span>

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

### <span data-ttu-id="f286a-143">-이름</span><span class="sxs-lookup"><span data-stu-id="f286a-143">-Name</span></span>
<span data-ttu-id="f286a-144">이 cmdlet이 수정 하는 정책 할당의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f286a-144">Specifies the name of the policy assignment that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="f286a-145">-NotScope</span><span class="sxs-lookup"><span data-stu-id="f286a-145">-NotScope</span></span>
<span data-ttu-id="f286a-146">정책 할당이 범위를 지정 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f286a-146">The policy assignment not scopes.</span></span>

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

### <span data-ttu-id="f286a-147">-Pre</span><span class="sxs-lookup"><span data-stu-id="f286a-147">-Pre</span></span>
<span data-ttu-id="f286a-148">이 cmdlet이 사용할 버전을 자동으로 결정 하는 경우 시험판 API 버전을 고려 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="f286a-148">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="f286a-149">-범위</span><span class="sxs-lookup"><span data-stu-id="f286a-149">-Scope</span></span>
<span data-ttu-id="f286a-150">정책이 적용 되는 범위를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f286a-150">Specifies the scope at which the policy is applied.</span></span>

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

### <span data-ttu-id="f286a-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f286a-151">CommonParameters</span></span>
<span data-ttu-id="f286a-152">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f286a-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f286a-153">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f286a-153">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f286a-154">입력</span><span class="sxs-lookup"><span data-stu-id="f286a-154">INPUTS</span></span>

### <span data-ttu-id="f286a-155">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="f286a-155">System.String</span></span>

### <span data-ttu-id="f286a-156">System.webserver []</span><span class="sxs-lookup"><span data-stu-id="f286a-156">System.String[]</span></span>

## <span data-ttu-id="f286a-157">출력</span><span class="sxs-lookup"><span data-stu-id="f286a-157">OUTPUTS</span></span>

### <span data-ttu-id="f286a-158">System.webserver. 자동. PSObject</span><span class="sxs-lookup"><span data-stu-id="f286a-158">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="f286a-159">상속자</span><span class="sxs-lookup"><span data-stu-id="f286a-159">NOTES</span></span>

## <span data-ttu-id="f286a-160">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f286a-160">RELATED LINKS</span></span>

[<span data-ttu-id="f286a-161">Get-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="f286a-161">Get-AzPolicyAssignment</span></span>](./Get-AzPolicyAssignment.md)

[<span data-ttu-id="f286a-162">새로운 AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="f286a-162">New-AzPolicyAssignment</span></span>](./New-AzPolicyAssignment.md)

[<span data-ttu-id="f286a-163">제거-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="f286a-163">Remove-AzPolicyAssignment</span></span>](./Remove-AzPolicyAssignment.md)


