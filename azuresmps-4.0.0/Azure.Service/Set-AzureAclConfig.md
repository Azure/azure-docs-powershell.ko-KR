---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: A9E43722-DEE2-4A5C-A3F6-8DA6612735AC
online version: ''
schema: 2.0.0
ms.openlocfilehash: 34e6e98c2bf506e8102287251e18dceda4dd0c7c
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046432"
---
# <span data-ttu-id="87a7d-101">Set-AzureAclConfig</span><span class="sxs-lookup"><span data-stu-id="87a7d-101">Set-AzureAclConfig</span></span>

## <span data-ttu-id="87a7d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="87a7d-102">SYNOPSIS</span></span>
<span data-ttu-id="87a7d-103">ACL 구성 개체를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="87a7d-103">Modifies an ACL configuration object.</span></span>

## <span data-ttu-id="87a7d-104">구문과</span><span class="sxs-lookup"><span data-stu-id="87a7d-104">SYNTAX</span></span>

### <span data-ttu-id="87a7d-105">AddRule</span><span class="sxs-lookup"><span data-stu-id="87a7d-105">AddRule</span></span>
```
Set-AzureAclConfig [-AddRule] [-Action] <String> [-RemoteSubnet] <String> [[-Order] <Int32>]
 [[-Description] <String>] -ACL <NetworkAclObject> [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="87a7d-106">RemoveRule</span><span class="sxs-lookup"><span data-stu-id="87a7d-106">RemoveRule</span></span>
```
Set-AzureAclConfig [-RemoveRule] [-RuleId] <Int32> -ACL <NetworkAclObject>
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="87a7d-107">SetRule</span><span class="sxs-lookup"><span data-stu-id="87a7d-107">SetRule</span></span>
```
Set-AzureAclConfig [-SetRule] [-RuleId] <Int32> [[-Action] <String>] [[-RemoteSubnet] <String>]
 [[-Order] <Int32>] [[-Description] <String>] -ACL <NetworkAclObject> [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="87a7d-108">설명은</span><span class="sxs-lookup"><span data-stu-id="87a7d-108">DESCRIPTION</span></span>
<span data-ttu-id="87a7d-109">**Set AzureAclConfig** cmdlet은 기존 Azure 가상 컴퓨터 구성에서 ACL (액세스 제어 목록) 구성 개체를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="87a7d-109">The **Set-AzureAclConfig** cmdlet modifies an access control list (ACL) configuration object from an existing Azure virtual machine configuration.</span></span>

## <span data-ttu-id="87a7d-110">예제의</span><span class="sxs-lookup"><span data-stu-id="87a7d-110">EXAMPLES</span></span>

### <span data-ttu-id="87a7d-111">예제 1: 새 ACL 구성에 규칙 추가</span><span class="sxs-lookup"><span data-stu-id="87a7d-111">Example 1: Add a rule to a new ACL configuration</span></span>
```
PS C:\> $Acl = New-AzureAclConfig
PS C:\> Set-AzureAclConfig -AddRule -ACL $Acl -Action Permit -RemoteSubnet "172.0.0.0/8" -Order 100 -Description "Permit ACL rule"
```

<span data-ttu-id="87a7d-112">첫 번째 명령은 ACL 구성을 만든 다음 $Acl 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="87a7d-112">The first command creates an ACL configuration, and then stores it in the $Acl variable.</span></span>

<span data-ttu-id="87a7d-113">두 번째 명령은 $Acl에 저장 된 구성에 새 규칙을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="87a7d-113">The second command adds a new rule to the configuration stored in $Acl.</span></span>
<span data-ttu-id="87a7d-114">명령에 규칙에 대 한 동작, 서브넷, 순서, 설명을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="87a7d-114">The command specifies an action, subnet, order, and description for the rule.</span></span>

### <span data-ttu-id="87a7d-115">예제 2: ACL 구성에서 규칙 수정</span><span class="sxs-lookup"><span data-stu-id="87a7d-115">Example 2: Modify a rule in an ACL configuration</span></span>
```
PS C:\> $Acl = Get-AzureVM -ServiceName "ContosoService" -Name "VirtualMachine07" | Get-AzureAclConfig -EndpointName "Web"
PS C:\> Set-AzureAclConfig -SetRule -RuleId 0 -ACL $Acl -Order 102 -Description "Web endpoint rule"
PS C:\> Get-AzureVM -ServiceName "ContosoService" -Name "VirtualMachine07" | Set-AzureEndpoint -ACL $Acl -Name "Web" | Update-AzureVM
```

<span data-ttu-id="87a7d-116">첫 번째 명령은 **VirtualMachine07 cmdlet을 사용 하 여 ContosoService** 이라는 이름의 서비스에서 가상 컴퓨터 이름을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="87a7d-116">The first command gets the virtual machine named VirtualMachine07 in the service named ContosoService by using the **Get-AzureVM** cmdlet.</span></span>
<span data-ttu-id="87a7d-117">이 명령은 파이프라인 연산자를 사용 하 여 해당 개체를 **Get AzureAclConfig** cmdlet에 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="87a7d-117">The command passes that object to the **Get-AzureAclConfig** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="87a7d-118">해당 cmdlet은 Web 이라는 끝점에 대 한 ACL 구성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="87a7d-118">That cmdlet gets the ACL configuration for the endpoint named Web.</span></span>
<span data-ttu-id="87a7d-119">명령은 $Acl 변수에 해당 ACL 구성 개체를 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="87a7d-119">The command stores that ACL configuration object in the $Acl variable.</span></span>

<span data-ttu-id="87a7d-120">두 번째 명령은 ID가 0 인 규칙을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="87a7d-120">The second command modifies the rule that has the ID of 0.</span></span>
<span data-ttu-id="87a7d-121">명령에서 규칙의 순서와 설명을 변경 합니다.</span><span class="sxs-lookup"><span data-stu-id="87a7d-121">The command changes the order and the description of the rule.</span></span>

<span data-ttu-id="87a7d-122">마지막 명령은 **Set AzureEndpoint** cmdlet을 사용 하 여 해당 가상 컴퓨터에 대 한 ACL 구성 개체를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="87a7d-122">The final command sets the ACL configuration object for that virtual machine by using the **Set-AzureEndpoint** cmdlet.</span></span>
<span data-ttu-id="87a7d-123">또한이 명령은 해당 가상 컴퓨터를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="87a7d-123">The command also updates that virtual machine.</span></span>

### <span data-ttu-id="87a7d-124">예제 3: ACL 구성에서 규칙 제거</span><span class="sxs-lookup"><span data-stu-id="87a7d-124">Example 3: Remove a rule from an ACL configuration</span></span>
```
PS C:\> $Acl = Get-AzureVM -ServiceName "ContosoService" -Name "VirtualMachine07" | Get-AzureAclConfig -EndpointName "Web"
PS C:\> Set-AzureAclConfig -RemoveRule -ID 0 -ACL $Acl
PS C:\> Get-AzureVM -ServiceName "ContosoService" -Name "VirtualMachine07" | Set-AzureEndpoint -ACL $Acl -Name "Web" | Update-AzureVM
```

<span data-ttu-id="87a7d-125">첫 번째 명령은 $Acl 변수에 ACL 구성 개체를 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="87a7d-125">The first command stores an ACL configuration object in the $Acl variable.</span></span>
<span data-ttu-id="87a7d-126">이는 이전 예제와 동일 합니다.</span><span class="sxs-lookup"><span data-stu-id="87a7d-126">This is the same as the previous example.</span></span>

<span data-ttu-id="87a7d-127">두 번째 명령은 $Acl의 ACL 구성에서 ID가 0 인 규칙을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="87a7d-127">The second command removes the rule that has the ID 0 from the ACL configuration in $Acl.</span></span>

<span data-ttu-id="87a7d-128">마지막 명령은 가상 컴퓨터에 대 한 ACL 구성 개체를 설정 하 고 해당 가상 컴퓨터를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="87a7d-128">The final command sets the ACL configuration object for the virtual machine and updates that virtual machine.</span></span>
<span data-ttu-id="87a7d-129">이는 이전 예제와 동일 합니다.</span><span class="sxs-lookup"><span data-stu-id="87a7d-129">This is the same as the previous example.</span></span>

## <span data-ttu-id="87a7d-130">변수</span><span class="sxs-lookup"><span data-stu-id="87a7d-130">PARAMETERS</span></span>

### <span data-ttu-id="87a7d-131">-ACL</span><span class="sxs-lookup"><span data-stu-id="87a7d-131">-ACL</span></span>
<span data-ttu-id="87a7d-132">이 cmdlet이 수정 하는 ACL 구성 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="87a7d-132">Specifies an ACL configuration object that this cmdlet modifies.</span></span>

```yaml
Type: NetworkAclObject
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="87a7d-133">-작업</span><span class="sxs-lookup"><span data-stu-id="87a7d-133">-Action</span></span>
<span data-ttu-id="87a7d-134">이 cmdlet이 추가 하거나 수정 하는 규칙에 대 한 작업을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="87a7d-134">Specifies the action for the rule that this cmdlet adds or modifies.</span></span>
<span data-ttu-id="87a7d-135">유효한 값은 허용 및 거부입니다.</span><span class="sxs-lookup"><span data-stu-id="87a7d-135">Valid values are: Permit and Deny.</span></span>

```yaml
Type: String
Parameter Sets: AddRule
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: SetRule
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87a7d-136">-AddRule</span><span class="sxs-lookup"><span data-stu-id="87a7d-136">-AddRule</span></span>
<span data-ttu-id="87a7d-137">이 cmdlet이 ACL 구성에 규칙을 추가 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="87a7d-137">Indicates that this cmdlet adds a rule to the ACL configuration.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: AddRule
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87a7d-138">-설명</span><span class="sxs-lookup"><span data-stu-id="87a7d-138">-Description</span></span>
<span data-ttu-id="87a7d-139">이 cmdlet이 추가 하거나 수정 하는 규칙에 대 한 설명을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="87a7d-139">Specifies a description for the rule that this cmdlet adds or modifies.</span></span>

```yaml
Type: String
Parameter Sets: AddRule, SetRule
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87a7d-140">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="87a7d-140">-InformationAction</span></span>
<span data-ttu-id="87a7d-141">이 cmdlet이 정보 이벤트에 응답 하는 방법을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="87a7d-141">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="87a7d-142">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="87a7d-142">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="87a7d-143">하기로</span><span class="sxs-lookup"><span data-stu-id="87a7d-143">Continue</span></span>
- <span data-ttu-id="87a7d-144">숨기기</span><span class="sxs-lookup"><span data-stu-id="87a7d-144">Ignore</span></span>
- <span data-ttu-id="87a7d-145">Inquire</span><span class="sxs-lookup"><span data-stu-id="87a7d-145">Inquire</span></span>
- <span data-ttu-id="87a7d-146">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="87a7d-146">SilentlyContinue</span></span>
- <span data-ttu-id="87a7d-147">중지가</span><span class="sxs-lookup"><span data-stu-id="87a7d-147">Stop</span></span>
- <span data-ttu-id="87a7d-148">대기</span><span class="sxs-lookup"><span data-stu-id="87a7d-148">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87a7d-149">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="87a7d-149">-InformationVariable</span></span>
<span data-ttu-id="87a7d-150">정보 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="87a7d-150">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87a7d-151">-주문</span><span class="sxs-lookup"><span data-stu-id="87a7d-151">-Order</span></span>
<span data-ttu-id="87a7d-152">이 cmdlet이 추가 하거나 수정 하는 규칙의 처리 순서를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="87a7d-152">Specifies the processing order for the rule that this cmdlet adds or modifies.</span></span>

```yaml
Type: Int32
Parameter Sets: AddRule, SetRule
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87a7d-153">-RemoteSubnet</span><span class="sxs-lookup"><span data-stu-id="87a7d-153">-RemoteSubnet</span></span>
<span data-ttu-id="87a7d-154">이 cmdlet이 추가 하거나 수정 하는 규칙에 대 한 원격 서브넷을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="87a7d-154">Specifies the remote subnet for the rule that this cmdlet adds or modifies.</span></span>
<span data-ttu-id="87a7d-155">CIDR (클래스 없는 도메인간 라우팅) 형식의 주소를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="87a7d-155">Specifies an address in Classless Interdomain Routing (CIDR) format.</span></span>

```yaml
Type: String
Parameter Sets: AddRule
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: SetRule
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87a7d-156">-RemoveRule</span><span class="sxs-lookup"><span data-stu-id="87a7d-156">-RemoveRule</span></span>
<span data-ttu-id="87a7d-157">이 cmdlet이 ACL 구성에서 규칙을 제거 했음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="87a7d-157">Indicates that this cmdlet removes a rule from the ACL configuration.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: RemoveRule
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87a7d-158">-RuleId</span><span class="sxs-lookup"><span data-stu-id="87a7d-158">-RuleId</span></span>
<span data-ttu-id="87a7d-159">이 cmdlet이 ACL 구성에 대해 제거 하거나 수정 하는 규칙의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="87a7d-159">Specifies the ID of the rule that this cmdlet removes or modifies for the ACL configuration.</span></span>

```yaml
Type: Int32
Parameter Sets: RemoveRule, SetRule
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87a7d-160">-SetRule</span><span class="sxs-lookup"><span data-stu-id="87a7d-160">-SetRule</span></span>
<span data-ttu-id="87a7d-161">이 cmdlet이 ACL 구성의 규칙을 수정 하는 것을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="87a7d-161">Indicates that this cmdlet modifies a rule in the ACL configuration.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: SetRule
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87a7d-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87a7d-162">CommonParameters</span></span>
<span data-ttu-id="87a7d-163">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="87a7d-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87a7d-164">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="87a7d-164">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87a7d-165">입력</span><span class="sxs-lookup"><span data-stu-id="87a7d-165">INPUTS</span></span>

## <span data-ttu-id="87a7d-166">출력</span><span class="sxs-lookup"><span data-stu-id="87a7d-166">OUTPUTS</span></span>

## <span data-ttu-id="87a7d-167">상속자</span><span class="sxs-lookup"><span data-stu-id="87a7d-167">NOTES</span></span>

## <span data-ttu-id="87a7d-168">관련 링크</span><span class="sxs-lookup"><span data-stu-id="87a7d-168">RELATED LINKS</span></span>

[<span data-ttu-id="87a7d-169">Get-AzureAclConfig</span><span class="sxs-lookup"><span data-stu-id="87a7d-169">Get-AzureAclConfig</span></span>](./Get-AzureAclConfig.md)

[<span data-ttu-id="87a7d-170">다운로드-Add-azurevm</span><span class="sxs-lookup"><span data-stu-id="87a7d-170">Get-AzureVM</span></span>](./Get-AzureVM.md)

[<span data-ttu-id="87a7d-171">새 AzureAclConfig</span><span class="sxs-lookup"><span data-stu-id="87a7d-171">New-AzureAclConfig</span></span>](./New-AzureAclConfig.md)

[<span data-ttu-id="87a7d-172">-AzureAclConfig 제거</span><span class="sxs-lookup"><span data-stu-id="87a7d-172">Remove-AzureAclConfig</span></span>](./Remove-AzureAclConfig.md)

[<span data-ttu-id="87a7d-173">Set-AzureEndpoint</span><span class="sxs-lookup"><span data-stu-id="87a7d-173">Set-AzureEndpoint</span></span>](./Set-AzureEndpoint.md)

[<span data-ttu-id="87a7d-174">업데이트-Add-azurevm</span><span class="sxs-lookup"><span data-stu-id="87a7d-174">Update-AzureVM</span></span>](./Update-AzureVM.md)


