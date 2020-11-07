---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Remove-AzSecurityContact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzSecurityContact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzSecurityContact.md
ms.openlocfilehash: eac99fc2395408f2e140b3369a87e75928006f21
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93871661"
---
# <span data-ttu-id="73ee6-101">Remove-AzSecurityContact</span><span class="sxs-lookup"><span data-stu-id="73ee6-101">Remove-AzSecurityContact</span></span>

## <span data-ttu-id="73ee6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="73ee6-102">SYNOPSIS</span></span>
<span data-ttu-id="73ee6-103">보안 연락처를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="73ee6-103">Deletes a security contact.</span></span>

## <span data-ttu-id="73ee6-104">구문과</span><span class="sxs-lookup"><span data-stu-id="73ee6-104">SYNTAX</span></span>

### <span data-ttu-id="73ee6-105">구독 Levelresource (기본값)</span><span class="sxs-lookup"><span data-stu-id="73ee6-105">SubscriptionLevelResource (Default)</span></span>
```
Remove-AzSecurityContact -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="73ee6-106">리소스</span><span class="sxs-lookup"><span data-stu-id="73ee6-106">ResourceId</span></span>
```
Remove-AzSecurityContact -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="73ee6-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="73ee6-107">InputObject</span></span>
```
Remove-AzSecurityContact -InputObject <PSSecurityContact> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="73ee6-108">설명은</span><span class="sxs-lookup"><span data-stu-id="73ee6-108">DESCRIPTION</span></span>
<span data-ttu-id="73ee6-109">보안 연락처를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="73ee6-109">Deletes a security contact.</span></span>

## <span data-ttu-id="73ee6-110">예제의</span><span class="sxs-lookup"><span data-stu-id="73ee6-110">EXAMPLES</span></span>

### <span data-ttu-id="73ee6-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="73ee6-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzSecurityContact -Name "default1"
```

<span data-ttu-id="73ee6-112">"Default1" 보안 연락처를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="73ee6-112">Deletes the "default1" security contact</span></span>

## <span data-ttu-id="73ee6-113">변수</span><span class="sxs-lookup"><span data-stu-id="73ee6-113">PARAMETERS</span></span>

### <span data-ttu-id="73ee6-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="73ee6-114">-DefaultProfile</span></span>
<span data-ttu-id="73ee6-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="73ee6-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="73ee6-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="73ee6-116">-InputObject</span></span>
<span data-ttu-id="73ee6-117">입력 개체</span><span class="sxs-lookup"><span data-stu-id="73ee6-117">Input Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Security.Models.SecurityContacts.PSSecurityContact
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="73ee6-118">-이름</span><span class="sxs-lookup"><span data-stu-id="73ee6-118">-Name</span></span>
<span data-ttu-id="73ee6-119">리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="73ee6-119">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73ee6-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="73ee6-120">-PassThru</span></span>
<span data-ttu-id="73ee6-121">작업이 성공적으로 수행 되었는지 여부를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="73ee6-121">Return whether the operation was successful.</span></span>

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

### <span data-ttu-id="73ee6-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="73ee6-122">-ResourceId</span></span>
<span data-ttu-id="73ee6-123">리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="73ee6-123">Resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="73ee6-124">-확인</span><span class="sxs-lookup"><span data-stu-id="73ee6-124">-Confirm</span></span>
<span data-ttu-id="73ee6-125">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="73ee6-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="73ee6-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="73ee6-126">-WhatIf</span></span>
<span data-ttu-id="73ee6-127">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="73ee6-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="73ee6-128">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="73ee6-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="73ee6-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73ee6-129">CommonParameters</span></span>
<span data-ttu-id="73ee6-130">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="73ee6-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73ee6-131">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="73ee6-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73ee6-132">입력</span><span class="sxs-lookup"><span data-stu-id="73ee6-132">INPUTS</span></span>

### <span data-ttu-id="73ee6-133">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="73ee6-133">System.String</span></span>

### <span data-ttu-id="73ee6-134">Microsoft. Azure. m a m a 연락처. PSSecurityContact</span><span class="sxs-lookup"><span data-stu-id="73ee6-134">Microsoft.Azure.Commands.Security.Models.SecurityContacts.PSSecurityContact</span></span>

## <span data-ttu-id="73ee6-135">출력</span><span class="sxs-lookup"><span data-stu-id="73ee6-135">OUTPUTS</span></span>

### <span data-ttu-id="73ee6-136">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="73ee6-136">System.Boolean</span></span>

## <span data-ttu-id="73ee6-137">상속자</span><span class="sxs-lookup"><span data-stu-id="73ee6-137">NOTES</span></span>

## <span data-ttu-id="73ee6-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="73ee6-138">RELATED LINKS</span></span>
