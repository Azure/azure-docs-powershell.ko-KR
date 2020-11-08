---
external help file: ''
Module Name: Az.CustomProviders
online version: https://docs.microsoft.com/en-us/powershell/module/az.customproviders/remove-azcustomproviderassociation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/Remove-AzCustomProviderAssociation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/Remove-AzCustomProviderAssociation.md
ms.openlocfilehash: 708bac976e32c2af114576d971c05843fd58ef93
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94215059"
---
# <span data-ttu-id="b9e91-101">Remove-AzCustomProviderAssociation</span><span class="sxs-lookup"><span data-stu-id="b9e91-101">Remove-AzCustomProviderAssociation</span></span>

## <span data-ttu-id="b9e91-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b9e91-102">SYNOPSIS</span></span>
<span data-ttu-id="b9e91-103">연결을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="b9e91-103">Delete an association.</span></span>

## <span data-ttu-id="b9e91-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b9e91-104">SYNTAX</span></span>

### <span data-ttu-id="b9e91-105">삭제 (기본값)</span><span class="sxs-lookup"><span data-stu-id="b9e91-105">Delete (Default)</span></span>
```
Remove-AzCustomProviderAssociation -Name <String> -Scope <String> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="b9e91-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="b9e91-106">DeleteViaIdentity</span></span>
```
Remove-AzCustomProviderAssociation -InputObject <ICustomProvidersIdentity> [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="b9e91-107">설명은</span><span class="sxs-lookup"><span data-stu-id="b9e91-107">DESCRIPTION</span></span>
<span data-ttu-id="b9e91-108">연결을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="b9e91-108">Delete an association.</span></span>

## <span data-ttu-id="b9e91-109">예제의</span><span class="sxs-lookup"><span data-stu-id="b9e91-109">EXAMPLES</span></span>

### <span data-ttu-id="b9e91-110">예제 1: 사용자 지정 공급자 연결 제거</span><span class="sxs-lookup"><span data-stu-id="b9e91-110">Example 1: Remove a custom provider association.</span></span>
```powershell
PS C:\> PS C:\> Remove-AzCustomProviderAssociation -Scope $id -Name Namespace.Type
```

<span data-ttu-id="b9e91-111">사용자 지정 공급자 연결을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="b9e91-111">Remove a custom provider association.</span></span>

### <span data-ttu-id="b9e91-112">예제 2: 사용자 지정 공급자와 파이핑 연결 제거</span><span class="sxs-lookup"><span data-stu-id="b9e91-112">Example 2: Remove a custom provider association with Piping</span></span>
```powershell
PS C:\> PS C:\> Get-AzCustomProviderAssociation | Remove-AzCustomProviderAssociation -PassThru

True
```

<span data-ttu-id="b9e91-113">파이핑 및 PassThru 기능을 사용 하 여 성공 또는 실패를 나타내는 사용자 지정 공급자 연결을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="b9e91-113">Remove a custom provider association, using piping and the PassThru feature to indicate success or failure.</span></span>

## <span data-ttu-id="b9e91-114">변수</span><span class="sxs-lookup"><span data-stu-id="b9e91-114">PARAMETERS</span></span>

### <span data-ttu-id="b9e91-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b9e91-115">-AsJob</span></span>
<span data-ttu-id="b9e91-116">작업으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="b9e91-116">Run the command as a job</span></span>

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

### <span data-ttu-id="b9e91-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9e91-117">-DefaultProfile</span></span>
<span data-ttu-id="b9e91-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b9e91-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9e91-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b9e91-119">-InputObject</span></span>
<span data-ttu-id="b9e91-120">생성할 id 매개 변수는 INPUTOBJECT 속성에 대 한 참고 섹션을 참조 하 고 해시 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b9e91-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.ICustomProvidersIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b9e91-121">-이름</span><span class="sxs-lookup"><span data-stu-id="b9e91-121">-Name</span></span>
<span data-ttu-id="b9e91-122">연결의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b9e91-122">The name of the association.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: AssociationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9e91-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="b9e91-123">-NoWait</span></span>
<span data-ttu-id="b9e91-124">비동기적으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="b9e91-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="b9e91-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b9e91-125">-PassThru</span></span>
<span data-ttu-id="b9e91-126">명령이 성공 하면 true를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="b9e91-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="b9e91-127">-범위</span><span class="sxs-lookup"><span data-stu-id="b9e91-127">-Scope</span></span>
<span data-ttu-id="b9e91-128">연결의 범위입니다.</span><span class="sxs-lookup"><span data-stu-id="b9e91-128">The scope of the association.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9e91-129">-확인</span><span class="sxs-lookup"><span data-stu-id="b9e91-129">-Confirm</span></span>
<span data-ttu-id="b9e91-130">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="b9e91-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9e91-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b9e91-131">-WhatIf</span></span>
<span data-ttu-id="b9e91-132">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="b9e91-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b9e91-133">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b9e91-133">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9e91-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9e91-134">CommonParameters</span></span>
<span data-ttu-id="b9e91-135">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b9e91-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9e91-136">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="b9e91-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9e91-137">입력</span><span class="sxs-lookup"><span data-stu-id="b9e91-137">INPUTS</span></span>

### <span data-ttu-id="b9e91-138">ICustomProvidersIdentity (Microsoft. PowerShell. i m m</span><span class="sxs-lookup"><span data-stu-id="b9e91-138">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.ICustomProvidersIdentity</span></span>

## <span data-ttu-id="b9e91-139">출력</span><span class="sxs-lookup"><span data-stu-id="b9e91-139">OUTPUTS</span></span>

### <span data-ttu-id="b9e91-140">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="b9e91-140">System.Boolean</span></span>

## <span data-ttu-id="b9e91-141">상속자</span><span class="sxs-lookup"><span data-stu-id="b9e91-141">NOTES</span></span>

<span data-ttu-id="b9e91-142">별칭과</span><span class="sxs-lookup"><span data-stu-id="b9e91-142">ALIASES</span></span>

<span data-ttu-id="b9e91-143">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="b9e91-143">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="b9e91-144">아래 설명 된 매개 변수를 만들려면 적절 한 속성을 포함 하는 해시 테이블을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="b9e91-144">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="b9e91-145">해시 테이블에 대 한 자세한 내용은 Get-Help about_Hash_Tables를 실행 하세요.</span><span class="sxs-lookup"><span data-stu-id="b9e91-145">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="b9e91-146">INPUTOBJECT <ICustomProvidersIdentity> : Identity 매개 변수</span><span class="sxs-lookup"><span data-stu-id="b9e91-146">INPUTOBJECT <ICustomProvidersIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="b9e91-147">`[AssociationName <String>]`: 연결의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b9e91-147">`[AssociationName <String>]`: The name of the association.</span></span>
  - <span data-ttu-id="b9e91-148">`[Id <String>]`: 리소스 id 경로</span><span class="sxs-lookup"><span data-stu-id="b9e91-148">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="b9e91-149">`[ResourceGroupName <String>]`: 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b9e91-149">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="b9e91-150">`[ResourceProviderName <String>]`: 리소스 공급자의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b9e91-150">`[ResourceProviderName <String>]`: The name of the resource provider.</span></span>
  - <span data-ttu-id="b9e91-151">`[Scope <String>]`: 연결의 범위입니다.</span><span class="sxs-lookup"><span data-stu-id="b9e91-151">`[Scope <String>]`: The scope of the association.</span></span>
  - <span data-ttu-id="b9e91-152">`[SubscriptionId <String>]`: Azure 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="b9e91-152">`[SubscriptionId <String>]`: The Azure subscription ID.</span></span> <span data-ttu-id="b9e91-153">GUID 형식 문자열입니다 (예: 00000000-0000-0000-0000-000000000000).</span><span class="sxs-lookup"><span data-stu-id="b9e91-153">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

## <span data-ttu-id="b9e91-154">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b9e91-154">RELATED LINKS</span></span>

