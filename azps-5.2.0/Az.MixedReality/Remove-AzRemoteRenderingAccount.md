---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MixedReality.dll-Help.xml
Module Name: Az.MixedReality
online version: https://docs.microsoft.com/en-us/powershell/module/az.mixedreality/remove-azremoterenderingaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/Remove-AzRemoteRenderingAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/Remove-AzRemoteRenderingAccount.md
ms.openlocfilehash: bfcbaa723dc2d06d74ba4d515affd2f19a51ec3e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98339465"
---
# <span data-ttu-id="126c9-101">Remove-AzRemoteRenderingAccount</span><span class="sxs-lookup"><span data-stu-id="126c9-101">Remove-AzRemoteRenderingAccount</span></span>

## <span data-ttu-id="126c9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="126c9-102">SYNOPSIS</span></span>
<span data-ttu-id="126c9-103">원격 렌더링 계정 삭제</span><span class="sxs-lookup"><span data-stu-id="126c9-103">Delete Remote Rendering Account</span></span>

## <span data-ttu-id="126c9-104">구문</span><span class="sxs-lookup"><span data-stu-id="126c9-104">SYNTAX</span></span>

### <span data-ttu-id="126c9-105">DefaultParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="126c9-105">DefaultParameterSet (Default)</span></span>
```
Remove-AzRemoteRenderingAccount -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="126c9-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="126c9-106">ResourceIdParameterSet</span></span>
```
Remove-AzRemoteRenderingAccount -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="126c9-107">PipelineParameterSet</span><span class="sxs-lookup"><span data-stu-id="126c9-107">PipelineParameterSet</span></span>
```
Remove-AzRemoteRenderingAccount -InputObject <PSRemoteRenderingAccount> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="126c9-108">설명</span><span class="sxs-lookup"><span data-stu-id="126c9-108">DESCRIPTION</span></span>
<span data-ttu-id="126c9-109">특정 구독 및 리소스 그룹에서 지정된 원격 렌더링 계정을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="126c9-109">Delete specified Remote Rendering Account from certain Subscription and Resource Group.</span></span>

## <span data-ttu-id="126c9-110">예제</span><span class="sxs-lookup"><span data-stu-id="126c9-110">EXAMPLES</span></span>

### <span data-ttu-id="126c9-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="126c9-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzRemoteRenderingAccount -ResourceGroup rg1 -Name example
```

<span data-ttu-id="126c9-112">현재 구독 및 리소스 그룹 "rg1"에서 원격 렌더링 계정 "예제"를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="126c9-112">Delete Remote Rendering Account "example" from current Subscription and Resource Group "rg1".</span></span>

## <span data-ttu-id="126c9-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="126c9-113">PARAMETERS</span></span>

### <span data-ttu-id="126c9-114">-Confirm</span><span class="sxs-lookup"><span data-stu-id="126c9-114">-Confirm</span></span>
<span data-ttu-id="126c9-115">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="126c9-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="126c9-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="126c9-116">-DefaultProfile</span></span>
<span data-ttu-id="126c9-117">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="126c9-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="126c9-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="126c9-118">-InputObject</span></span>
<span data-ttu-id="126c9-119">사용자 지정 도메인 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="126c9-119">The custom domain object.</span></span>

```yaml
Type: PSRemoteRenderingAccount
Parameter Sets: PipelineParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="126c9-120">-Name</span><span class="sxs-lookup"><span data-stu-id="126c9-120">-Name</span></span>
<span data-ttu-id="126c9-121">원격 렌더링 계정 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="126c9-121">Remote Rendering Account Name.</span></span>

```yaml
Type: String
Parameter Sets: DefaultParameterSet
Aliases: RemoteRenderingAccountName, AccountName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="126c9-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="126c9-122">-PassThru</span></span>
<span data-ttu-id="126c9-123">지정된 경우 개체를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="126c9-123">Return object if specified.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="126c9-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="126c9-124">-ResourceGroupName</span></span>
<span data-ttu-id="126c9-125">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="126c9-125">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: DefaultParameterSet
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="126c9-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="126c9-126">-ResourceId</span></span>
<span data-ttu-id="126c9-127">원격 렌더링 계정의 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="126c9-127">Resource ID of Remote Rendering Account.</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="126c9-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="126c9-128">-WhatIf</span></span>
<span data-ttu-id="126c9-129">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="126c9-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="126c9-130">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="126c9-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="126c9-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="126c9-131">CommonParameters</span></span>
<span data-ttu-id="126c9-132">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="126c9-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="126c9-133">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="126c9-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="126c9-134">입력</span><span class="sxs-lookup"><span data-stu-id="126c9-134">INPUTS</span></span>

### <span data-ttu-id="126c9-135">System.String</span><span class="sxs-lookup"><span data-stu-id="126c9-135">System.String</span></span>

### <span data-ttu-id="126c9-136">Microsoft.Azure.Commands.MixedReality.RemoteRenderingAccount.PSRemoteRenderingAccount</span><span class="sxs-lookup"><span data-stu-id="126c9-136">Microsoft.Azure.Commands.MixedReality.RemoteRenderingAccount.PSRemoteRenderingAccount</span></span>

### <span data-ttu-id="126c9-137">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="126c9-137">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="126c9-138">출력</span><span class="sxs-lookup"><span data-stu-id="126c9-138">OUTPUTS</span></span>

### <span data-ttu-id="126c9-139">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="126c9-139">System.Boolean</span></span>

## <span data-ttu-id="126c9-140">참고 사항</span><span class="sxs-lookup"><span data-stu-id="126c9-140">NOTES</span></span>

## <span data-ttu-id="126c9-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="126c9-141">RELATED LINKS</span></span>
