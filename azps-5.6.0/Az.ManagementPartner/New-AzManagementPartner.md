---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ManagementPartner.dll-Help.xml
Module Name: Az.ManagementPartner
online version: https://docs.microsoft.com/powershell/module/az.managementpartner/new-azmanagementpartner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagementPartner/ManagementPartner/help/New-AzManagementPartner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagementPartner/ManagementPartner/help/New-AzManagementPartner.md
ms.openlocfilehash: 57d9f5d51cb2646274728f8b2f6d846bd954f2a7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101994219"
---
# <span data-ttu-id="0e63d-101">New-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="0e63d-101">New-AzManagementPartner</span></span>

## <span data-ttu-id="0e63d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0e63d-102">SYNOPSIS</span></span>
<span data-ttu-id="0e63d-103">Microsoft 파트너 네트워크(MPN) ID를 현재 인증된 사용자 또는 서비스 주체에 연결합니다.</span><span class="sxs-lookup"><span data-stu-id="0e63d-103">Associates a Microsoft Partner Network(MPN) ID to the current authenticated user or service principal.</span></span>

## <span data-ttu-id="0e63d-104">구문</span><span class="sxs-lookup"><span data-stu-id="0e63d-104">SYNTAX</span></span>

```
New-AzManagementPartner [-PartnerId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0e63d-105">설명</span><span class="sxs-lookup"><span data-stu-id="0e63d-105">DESCRIPTION</span></span>
<span data-ttu-id="0e63d-106">Microsoft 파트너 네트워크(MPN) ID를 현재 인증된 사용자 또는 서비스 주체에 연결합니다.</span><span class="sxs-lookup"><span data-stu-id="0e63d-106">Associates a Microsoft Partner Network(MPN) ID to the current authenticated user or service principal.</span></span>

## <span data-ttu-id="0e63d-107">예제</span><span class="sxs-lookup"><span data-stu-id="0e63d-107">EXAMPLES</span></span>

### <span data-ttu-id="0e63d-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="0e63d-108">Example 1</span></span>
```powershell
PS C:\> New-AzManagementPartner -PartnerId 4977985
PartnerId   : 4977985
PartnerName : Test_Test_DPORTest
TenantId    : 1b1121dd-6900-412a-af73-e8d44f81e1c1
ObjectId    : aa67f786-0552-423e-8849-244ed12bf581
State       : Active
```

<span data-ttu-id="0e63d-109">관리 파트너 추가</span><span class="sxs-lookup"><span data-stu-id="0e63d-109">Add a management partner</span></span>

## <span data-ttu-id="0e63d-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="0e63d-110">PARAMETERS</span></span>

### <span data-ttu-id="0e63d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0e63d-111">-DefaultProfile</span></span>
<span data-ttu-id="0e63d-112">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="0e63d-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0e63d-113">-PartnerId</span><span class="sxs-lookup"><span data-stu-id="0e63d-113">-PartnerId</span></span>
<span data-ttu-id="0e63d-114">관리 파트너 ID는 6자리 숫자입니다.</span><span class="sxs-lookup"><span data-stu-id="0e63d-114">The management partner id, it is a 6 digits number</span></span>

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

### <span data-ttu-id="0e63d-115">-확인</span><span class="sxs-lookup"><span data-stu-id="0e63d-115">-Confirm</span></span>
<span data-ttu-id="0e63d-116">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="0e63d-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0e63d-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0e63d-117">-WhatIf</span></span>
<span data-ttu-id="0e63d-118">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="0e63d-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0e63d-119">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0e63d-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0e63d-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0e63d-120">CommonParameters</span></span>
<span data-ttu-id="0e63d-121">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="0e63d-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0e63d-122">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="0e63d-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0e63d-123">입력</span><span class="sxs-lookup"><span data-stu-id="0e63d-123">INPUTS</span></span>

### <span data-ttu-id="0e63d-124">없음</span><span class="sxs-lookup"><span data-stu-id="0e63d-124">None</span></span>

## <span data-ttu-id="0e63d-125">출력</span><span class="sxs-lookup"><span data-stu-id="0e63d-125">OUTPUTS</span></span>

### <span data-ttu-id="0e63d-126">Microsoft.Azure.Commands.ManagementPartner.PSManagementPartner</span><span class="sxs-lookup"><span data-stu-id="0e63d-126">Microsoft.Azure.Commands.ManagementPartner.PSManagementPartner</span></span>

## <span data-ttu-id="0e63d-127">참고 사항</span><span class="sxs-lookup"><span data-stu-id="0e63d-127">NOTES</span></span>

## <span data-ttu-id="0e63d-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0e63d-128">RELATED LINKS</span></span>

[<span data-ttu-id="0e63d-129">Remove-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="0e63d-129">Remove-AzManagementPartner</span></span>](./Remove-AzManagementPartner.md)

[<span data-ttu-id="0e63d-130">Get-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="0e63d-130">Get-AzManagementPartner</span></span>](./Get-AzManagementPartner.md)

[<span data-ttu-id="0e63d-131">Update-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="0e63d-131">Update-AzManagementPartner</span></span>](./Update-AzManagementPartner.md)