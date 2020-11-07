---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ManagementPartner.dll-Help.xml
Module Name: Az.ManagementPartner
online version: https://docs.microsoft.com/en-us/powershell/module/az.managementpartner/update-azmanagementpartner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagementPartner/ManagementPartner/help/Update-AzManagementPartner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagementPartner/ManagementPartner/help/Update-AzManagementPartner.md
ms.openlocfilehash: 20d258cdd99da4e76fcf8394ebbe1aadd54f2fb1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93689387"
---
# <span data-ttu-id="a2fcb-101">Update-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="a2fcb-101">Update-AzManagementPartner</span></span>

## <span data-ttu-id="a2fcb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a2fcb-102">SYNOPSIS</span></span>
<span data-ttu-id="a2fcb-103">현재 인증 된 사용자 또는 서비스 주체의 MPN (Microsoft 파트너 네트워크) ID를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="a2fcb-103">Updates the Microsoft Partner Network(MPN) ID of the current authenticated user or service principal.</span></span>

## <span data-ttu-id="a2fcb-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a2fcb-104">SYNTAX</span></span>

```
Update-AzManagementPartner [-PartnerId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a2fcb-105">설명은</span><span class="sxs-lookup"><span data-stu-id="a2fcb-105">DESCRIPTION</span></span>
<span data-ttu-id="a2fcb-106">현재 인증 된 사용자 또는 서비스 주체의 MPN (Microsoft 파트너 네트워크) ID를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="a2fcb-106">Updates the Microsoft Partner Network(MPN) ID of the current authenticated user or service principal.</span></span>

## <span data-ttu-id="a2fcb-107">예제의</span><span class="sxs-lookup"><span data-stu-id="a2fcb-107">EXAMPLES</span></span>

### <span data-ttu-id="a2fcb-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="a2fcb-108">Example 1</span></span>
```powershell
PS C:\> Update-AzManagementPartner -PartnerId 4977985
PartnerId   : 4977985
PartnerName : Test_Test_DPORTest
TenantId    : 1b1121dd-6900-412a-af73-e8d44f81e1c1
ObjectId    : aa67f786-0552-423e-8849-244ed12bf581
State       : Active
```

<span data-ttu-id="a2fcb-109">새 항목으로 관리 파트너 업데이트</span><span class="sxs-lookup"><span data-stu-id="a2fcb-109">Update the management partner to a new one</span></span>

## <span data-ttu-id="a2fcb-110">변수</span><span class="sxs-lookup"><span data-stu-id="a2fcb-110">PARAMETERS</span></span>

### <span data-ttu-id="a2fcb-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a2fcb-111">-DefaultProfile</span></span>
<span data-ttu-id="a2fcb-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a2fcb-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a2fcb-113">-(또는)-(Id)</span><span class="sxs-lookup"><span data-stu-id="a2fcb-113">-PartnerId</span></span>
<span data-ttu-id="a2fcb-114">관리 파트너 id로 6 자리 숫자입니다.</span><span class="sxs-lookup"><span data-stu-id="a2fcb-114">The management partner id, it is a 6 digits number</span></span>

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

### <span data-ttu-id="a2fcb-115">-확인</span><span class="sxs-lookup"><span data-stu-id="a2fcb-115">-Confirm</span></span>
<span data-ttu-id="a2fcb-116">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="a2fcb-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a2fcb-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a2fcb-117">-WhatIf</span></span>
<span data-ttu-id="a2fcb-118">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="a2fcb-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a2fcb-119">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a2fcb-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a2fcb-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2fcb-120">CommonParameters</span></span>
<span data-ttu-id="a2fcb-121">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a2fcb-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2fcb-122">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a2fcb-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2fcb-123">입력</span><span class="sxs-lookup"><span data-stu-id="a2fcb-123">INPUTS</span></span>

### <span data-ttu-id="a2fcb-124">않아야</span><span class="sxs-lookup"><span data-stu-id="a2fcb-124">None</span></span>

## <span data-ttu-id="a2fcb-125">출력</span><span class="sxs-lookup"><span data-stu-id="a2fcb-125">OUTPUTS</span></span>

### <span data-ttu-id="a2fcb-126">Microsoft Azure. PSManagementPartner</span><span class="sxs-lookup"><span data-stu-id="a2fcb-126">Microsoft.Azure.Commands.ManagementPartner.PSManagementPartner</span></span>

## <span data-ttu-id="a2fcb-127">상속자</span><span class="sxs-lookup"><span data-stu-id="a2fcb-127">NOTES</span></span>

## <span data-ttu-id="a2fcb-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a2fcb-128">RELATED LINKS</span></span>

[<span data-ttu-id="a2fcb-129">제거-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="a2fcb-129">Remove-AzManagementPartner</span></span>](./Remove-AzManagementPartner.md)

[<span data-ttu-id="a2fcb-130">새로운 AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="a2fcb-130">New-AzManagementPartner</span></span>](./New-AzManagementPartner.md)

[<span data-ttu-id="a2fcb-131">Get-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="a2fcb-131">Get-AzManagementPartner</span></span>](./Get-AzManagementPartner.md)