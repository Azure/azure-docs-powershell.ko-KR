---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Remove-AzSecurityContact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzSecurityContact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzSecurityContact.md
ms.openlocfilehash: b4cbecd2e29a0b70c7e62194df2364b22b33b462
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100208264"
---
# <span data-ttu-id="bad0e-101">Remove-AzSecurityContact</span><span class="sxs-lookup"><span data-stu-id="bad0e-101">Remove-AzSecurityContact</span></span>

## <span data-ttu-id="bad0e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bad0e-102">SYNOPSIS</span></span>
<span data-ttu-id="bad0e-103">보안 연락처를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="bad0e-103">Deletes a security contact.</span></span>

## <span data-ttu-id="bad0e-104">구문</span><span class="sxs-lookup"><span data-stu-id="bad0e-104">SYNTAX</span></span>

### <span data-ttu-id="bad0e-105">SubscriptionLevelResource(기본값)</span><span class="sxs-lookup"><span data-stu-id="bad0e-105">SubscriptionLevelResource (Default)</span></span>
```
Remove-AzSecurityContact -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bad0e-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="bad0e-106">ResourceId</span></span>
```
Remove-AzSecurityContact -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bad0e-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="bad0e-107">InputObject</span></span>
```
Remove-AzSecurityContact -InputObject <PSSecurityContact> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bad0e-108">설명</span><span class="sxs-lookup"><span data-stu-id="bad0e-108">DESCRIPTION</span></span>
<span data-ttu-id="bad0e-109">보안 연락처를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="bad0e-109">Deletes a security contact.</span></span>

## <span data-ttu-id="bad0e-110">예제</span><span class="sxs-lookup"><span data-stu-id="bad0e-110">EXAMPLES</span></span>

### <span data-ttu-id="bad0e-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="bad0e-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzSecurityContact -Name "default1"
```

<span data-ttu-id="bad0e-112">"default1" 보안 연락처를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="bad0e-112">Deletes the "default1" security contact</span></span>

## <span data-ttu-id="bad0e-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bad0e-113">PARAMETERS</span></span>

### <span data-ttu-id="bad0e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bad0e-114">-DefaultProfile</span></span>
<span data-ttu-id="bad0e-115">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="bad0e-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bad0e-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bad0e-116">-InputObject</span></span>
<span data-ttu-id="bad0e-117">입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="bad0e-117">Input Object.</span></span>

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

### <span data-ttu-id="bad0e-118">-Name</span><span class="sxs-lookup"><span data-stu-id="bad0e-118">-Name</span></span>
<span data-ttu-id="bad0e-119">리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="bad0e-119">Resource name.</span></span>

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

### <span data-ttu-id="bad0e-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bad0e-120">-PassThru</span></span>
<span data-ttu-id="bad0e-121">작업이 성공한지 여부를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="bad0e-121">Return whether the operation was successful.</span></span>

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

### <span data-ttu-id="bad0e-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bad0e-122">-ResourceId</span></span>
<span data-ttu-id="bad0e-123">리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="bad0e-123">Resource ID.</span></span>

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

### <span data-ttu-id="bad0e-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bad0e-124">-Confirm</span></span>
<span data-ttu-id="bad0e-125">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="bad0e-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bad0e-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bad0e-126">-WhatIf</span></span>
<span data-ttu-id="bad0e-127">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="bad0e-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="bad0e-128">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="bad0e-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bad0e-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bad0e-129">CommonParameters</span></span>
<span data-ttu-id="bad0e-130">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="bad0e-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bad0e-131">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="bad0e-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bad0e-132">입력</span><span class="sxs-lookup"><span data-stu-id="bad0e-132">INPUTS</span></span>

### <span data-ttu-id="bad0e-133">System.String</span><span class="sxs-lookup"><span data-stu-id="bad0e-133">System.String</span></span>

### <span data-ttu-id="bad0e-134">Microsoft.Azure.Commands.Security.Models.SecurityContacts.PSSecurityContact</span><span class="sxs-lookup"><span data-stu-id="bad0e-134">Microsoft.Azure.Commands.Security.Models.SecurityContacts.PSSecurityContact</span></span>

## <span data-ttu-id="bad0e-135">출력</span><span class="sxs-lookup"><span data-stu-id="bad0e-135">OUTPUTS</span></span>

### <span data-ttu-id="bad0e-136">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="bad0e-136">System.Boolean</span></span>

## <span data-ttu-id="bad0e-137">참고 사항</span><span class="sxs-lookup"><span data-stu-id="bad0e-137">NOTES</span></span>

## <span data-ttu-id="bad0e-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="bad0e-138">RELATED LINKS</span></span>
