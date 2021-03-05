---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/powershell/module/az.security/Remove-AzSecurityContact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzSecurityContact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzSecurityContact.md
ms.openlocfilehash: f8b96d8441e9a0b3a5f9b9bc3c775da7d71f12c8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101992418"
---
# <span data-ttu-id="62846-101">Remove-AzSecurityContact</span><span class="sxs-lookup"><span data-stu-id="62846-101">Remove-AzSecurityContact</span></span>

## <span data-ttu-id="62846-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="62846-102">SYNOPSIS</span></span>
<span data-ttu-id="62846-103">보안 연락처를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="62846-103">Deletes a security contact.</span></span>

## <span data-ttu-id="62846-104">구문</span><span class="sxs-lookup"><span data-stu-id="62846-104">SYNTAX</span></span>

### <span data-ttu-id="62846-105">SubscriptionLevelResource(기본값)</span><span class="sxs-lookup"><span data-stu-id="62846-105">SubscriptionLevelResource (Default)</span></span>
```
Remove-AzSecurityContact -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="62846-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="62846-106">ResourceId</span></span>
```
Remove-AzSecurityContact -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="62846-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="62846-107">InputObject</span></span>
```
Remove-AzSecurityContact -InputObject <PSSecurityContact> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="62846-108">설명</span><span class="sxs-lookup"><span data-stu-id="62846-108">DESCRIPTION</span></span>
<span data-ttu-id="62846-109">보안 연락처를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="62846-109">Deletes a security contact.</span></span>

## <span data-ttu-id="62846-110">예제</span><span class="sxs-lookup"><span data-stu-id="62846-110">EXAMPLES</span></span>

### <span data-ttu-id="62846-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="62846-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzSecurityContact -Name "default1"
```

<span data-ttu-id="62846-112">"default1" 보안 연락처를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="62846-112">Deletes the "default1" security contact</span></span>

## <span data-ttu-id="62846-113">매개 변수</span><span class="sxs-lookup"><span data-stu-id="62846-113">PARAMETERS</span></span>

### <span data-ttu-id="62846-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62846-114">-DefaultProfile</span></span>
<span data-ttu-id="62846-115">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="62846-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="62846-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="62846-116">-InputObject</span></span>
<span data-ttu-id="62846-117">입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="62846-117">Input Object.</span></span>

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

### <span data-ttu-id="62846-118">-Name</span><span class="sxs-lookup"><span data-stu-id="62846-118">-Name</span></span>
<span data-ttu-id="62846-119">리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="62846-119">Resource name.</span></span>

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

### <span data-ttu-id="62846-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="62846-120">-PassThru</span></span>
<span data-ttu-id="62846-121">작업이 성공한지 여부를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="62846-121">Return whether the operation was successful.</span></span>

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

### <span data-ttu-id="62846-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="62846-122">-ResourceId</span></span>
<span data-ttu-id="62846-123">리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="62846-123">Resource ID.</span></span>

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

### <span data-ttu-id="62846-124">-확인</span><span class="sxs-lookup"><span data-stu-id="62846-124">-Confirm</span></span>
<span data-ttu-id="62846-125">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="62846-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="62846-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="62846-126">-WhatIf</span></span>
<span data-ttu-id="62846-127">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="62846-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="62846-128">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="62846-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="62846-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62846-129">CommonParameters</span></span>
<span data-ttu-id="62846-130">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="62846-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62846-131">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="62846-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62846-132">입력</span><span class="sxs-lookup"><span data-stu-id="62846-132">INPUTS</span></span>

### <span data-ttu-id="62846-133">System.String</span><span class="sxs-lookup"><span data-stu-id="62846-133">System.String</span></span>

### <span data-ttu-id="62846-134">Microsoft.Azure.Commands.Security.Models.SecurityContacts.PSSecurityContact</span><span class="sxs-lookup"><span data-stu-id="62846-134">Microsoft.Azure.Commands.Security.Models.SecurityContacts.PSSecurityContact</span></span>

## <span data-ttu-id="62846-135">출력</span><span class="sxs-lookup"><span data-stu-id="62846-135">OUTPUTS</span></span>

### <span data-ttu-id="62846-136">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="62846-136">System.Boolean</span></span>

## <span data-ttu-id="62846-137">참고 사항</span><span class="sxs-lookup"><span data-stu-id="62846-137">NOTES</span></span>

## <span data-ttu-id="62846-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="62846-138">RELATED LINKS</span></span>
