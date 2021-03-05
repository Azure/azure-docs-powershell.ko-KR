---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ManagementPartner.dll-Help.xml
Module Name: Az.ManagementPartner
online version: https://docs.microsoft.com/powershell/module/az.managementpartner/remove-azmanagementpartner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagementPartner/ManagementPartner/help/Remove-AzManagementPartner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagementPartner/ManagementPartner/help/Remove-AzManagementPartner.md
ms.openlocfilehash: 7a213cbe8acacebc0f6e513e264432ca2ba08cf3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101990075"
---
# <span data-ttu-id="1a226-101">Remove-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="1a226-101">Remove-AzManagementPartner</span></span>

## <span data-ttu-id="1a226-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1a226-102">SYNOPSIS</span></span>
<span data-ttu-id="1a226-103">현재 인증된 사용자 또는 서비스 주체의 MPN(Microsoft 파트너 네트워크) ID를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="1a226-103">Delete the Microsoft Partner Network(MPN) ID of the current authenticated user or service principal.</span></span>

## <span data-ttu-id="1a226-104">구문</span><span class="sxs-lookup"><span data-stu-id="1a226-104">SYNTAX</span></span>

```
Remove-AzManagementPartner [-PartnerId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1a226-105">설명</span><span class="sxs-lookup"><span data-stu-id="1a226-105">DESCRIPTION</span></span>
<span data-ttu-id="1a226-106">현재 인증된 사용자 또는 서비스 주체의 MPN(Microsoft 파트너 네트워크) ID를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="1a226-106">Delete the Microsoft Partner Network(MPN) ID of the current authenticated user or service principal.</span></span>

## <span data-ttu-id="1a226-107">예제</span><span class="sxs-lookup"><span data-stu-id="1a226-107">EXAMPLES</span></span>

### <span data-ttu-id="1a226-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="1a226-108">Example 1</span></span>
```powershell
PS C:\>Remove-AzManagementPartner -PartnerId 123457 -PassThru
true
```

<span data-ttu-id="1a226-109">관리 파트너 제거</span><span class="sxs-lookup"><span data-stu-id="1a226-109">Remove management partner</span></span>

## <span data-ttu-id="1a226-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="1a226-110">PARAMETERS</span></span>

### <span data-ttu-id="1a226-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1a226-111">-DefaultProfile</span></span>
<span data-ttu-id="1a226-112">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="1a226-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1a226-113">-PartnerId</span><span class="sxs-lookup"><span data-stu-id="1a226-113">-PartnerId</span></span>
<span data-ttu-id="1a226-114">관리 파트너 ID는 6자리 숫자입니다.</span><span class="sxs-lookup"><span data-stu-id="1a226-114">The management partner id, it is a 6 digits number</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1a226-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1a226-115">-PassThru</span></span>
<span data-ttu-id="1a226-116">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="1a226-116">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="1a226-117">-확인</span><span class="sxs-lookup"><span data-stu-id="1a226-117">-Confirm</span></span>
<span data-ttu-id="1a226-118">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="1a226-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1a226-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1a226-119">-WhatIf</span></span>
<span data-ttu-id="1a226-120">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="1a226-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1a226-121">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1a226-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1a226-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a226-122">CommonParameters</span></span>
<span data-ttu-id="1a226-123">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="1a226-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a226-124">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="1a226-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a226-125">입력</span><span class="sxs-lookup"><span data-stu-id="1a226-125">INPUTS</span></span>

### <span data-ttu-id="1a226-126">없음</span><span class="sxs-lookup"><span data-stu-id="1a226-126">None</span></span>

## <span data-ttu-id="1a226-127">출력</span><span class="sxs-lookup"><span data-stu-id="1a226-127">OUTPUTS</span></span>

### <span data-ttu-id="1a226-128">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="1a226-128">System.Boolean</span></span>

## <span data-ttu-id="1a226-129">참고 사항</span><span class="sxs-lookup"><span data-stu-id="1a226-129">NOTES</span></span>

## <span data-ttu-id="1a226-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1a226-130">RELATED LINKS</span></span>

[<span data-ttu-id="1a226-131">New-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="1a226-131">New-AzManagementPartner</span></span>](./New-AzManagementPartner.md)

[<span data-ttu-id="1a226-132">Get-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="1a226-132">Get-AzManagementPartner</span></span>](./Get-AzManagementPartner.md)

[<span data-ttu-id="1a226-133">Update-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="1a226-133">Update-AzManagementPartner</span></span>](./Update-AzManagementPartner.md)