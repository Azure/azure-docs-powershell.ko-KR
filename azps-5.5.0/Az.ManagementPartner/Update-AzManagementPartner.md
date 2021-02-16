---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ManagementPartner.dll-Help.xml
Module Name: Az.ManagementPartner
online version: https://docs.microsoft.com/en-us/powershell/module/az.managementpartner/update-azmanagementpartner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagementPartner/ManagementPartner/help/Update-AzManagementPartner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagementPartner/ManagementPartner/help/Update-AzManagementPartner.md
ms.openlocfilehash: 326e16ff2f5bca8ca5ae987ebedf12cace87e11d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100180284"
---
# <span data-ttu-id="99455-101">Update-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="99455-101">Update-AzManagementPartner</span></span>

## <span data-ttu-id="99455-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="99455-102">SYNOPSIS</span></span>
<span data-ttu-id="99455-103">현재 인증된 사용자 또는 서비스 주체의 MPN(Microsoft 파트너 네트워크) ID를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="99455-103">Updates the Microsoft Partner Network(MPN) ID of the current authenticated user or service principal.</span></span>

## <span data-ttu-id="99455-104">구문</span><span class="sxs-lookup"><span data-stu-id="99455-104">SYNTAX</span></span>

```
Update-AzManagementPartner [-PartnerId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="99455-105">설명</span><span class="sxs-lookup"><span data-stu-id="99455-105">DESCRIPTION</span></span>
<span data-ttu-id="99455-106">현재 인증된 사용자 또는 서비스 주체의 MPN(Microsoft 파트너 네트워크) ID를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="99455-106">Updates the Microsoft Partner Network(MPN) ID of the current authenticated user or service principal.</span></span>

## <span data-ttu-id="99455-107">예제</span><span class="sxs-lookup"><span data-stu-id="99455-107">EXAMPLES</span></span>

### <span data-ttu-id="99455-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="99455-108">Example 1</span></span>
```powershell
PS C:\> Update-AzManagementPartner -PartnerId 4977985
PartnerId   : 4977985
PartnerName : Test_Test_DPORTest
TenantId    : 1b1121dd-6900-412a-af73-e8d44f81e1c1
ObjectId    : aa67f786-0552-423e-8849-244ed12bf581
State       : Active
```

<span data-ttu-id="99455-109">관리 파트너를 새 파트너로 업데이트</span><span class="sxs-lookup"><span data-stu-id="99455-109">Update the management partner to a new one</span></span>

## <span data-ttu-id="99455-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="99455-110">PARAMETERS</span></span>

### <span data-ttu-id="99455-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="99455-111">-DefaultProfile</span></span>
<span data-ttu-id="99455-112">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="99455-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="99455-113">-PartnerId</span><span class="sxs-lookup"><span data-stu-id="99455-113">-PartnerId</span></span>
<span data-ttu-id="99455-114">관리 파트너 ID로, 6자리 숫자입니다.</span><span class="sxs-lookup"><span data-stu-id="99455-114">The management partner id, it is a 6 digits number</span></span>

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

### <span data-ttu-id="99455-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="99455-115">-Confirm</span></span>
<span data-ttu-id="99455-116">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="99455-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="99455-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="99455-117">-WhatIf</span></span>
<span data-ttu-id="99455-118">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="99455-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="99455-119">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="99455-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="99455-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99455-120">CommonParameters</span></span>
<span data-ttu-id="99455-121">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="99455-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99455-122">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="99455-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99455-123">입력</span><span class="sxs-lookup"><span data-stu-id="99455-123">INPUTS</span></span>

### <span data-ttu-id="99455-124">없음</span><span class="sxs-lookup"><span data-stu-id="99455-124">None</span></span>

## <span data-ttu-id="99455-125">출력</span><span class="sxs-lookup"><span data-stu-id="99455-125">OUTPUTS</span></span>

### <span data-ttu-id="99455-126">Microsoft.Azure.Commands.ManagementPartner.PSManagementPartner</span><span class="sxs-lookup"><span data-stu-id="99455-126">Microsoft.Azure.Commands.ManagementPartner.PSManagementPartner</span></span>

## <span data-ttu-id="99455-127">참고 사항</span><span class="sxs-lookup"><span data-stu-id="99455-127">NOTES</span></span>

## <span data-ttu-id="99455-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="99455-128">RELATED LINKS</span></span>

[<span data-ttu-id="99455-129">Remove-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="99455-129">Remove-AzManagementPartner</span></span>](./Remove-AzManagementPartner.md)

[<span data-ttu-id="99455-130">New-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="99455-130">New-AzManagementPartner</span></span>](./New-AzManagementPartner.md)

[<span data-ttu-id="99455-131">Get-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="99455-131">Get-AzManagementPartner</span></span>](./Get-AzManagementPartner.md)