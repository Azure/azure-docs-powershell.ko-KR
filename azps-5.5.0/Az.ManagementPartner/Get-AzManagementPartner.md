---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ManagementPartner.dll-Help.xml
Module Name: Az.ManagementPartner
online version: https://docs.microsoft.com/en-us/powershell/module/az.managementpartner/get-azmanagementpartner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagementPartner/ManagementPartner/help/Get-AzManagementPartner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagementPartner/ManagementPartner/help/Get-AzManagementPartner.md
ms.openlocfilehash: 1031c9c8828969d16097953aa7440e2c8c0a8c1b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100180289"
---
# <span data-ttu-id="4bef8-101">Get-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="4bef8-101">Get-AzManagementPartner</span></span>

## <span data-ttu-id="4bef8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4bef8-102">SYNOPSIS</span></span>
<span data-ttu-id="4bef8-103">현재 인증된 사용자 또는 서비스 주체의 MPN(Microsoft 파트너 네트워크) ID를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="4bef8-103">Gets the Microsoft Partner Network(MPN) ID of the current authenticated user or service principal.</span></span>

## <span data-ttu-id="4bef8-104">구문</span><span class="sxs-lookup"><span data-stu-id="4bef8-104">SYNTAX</span></span>

```
Get-AzManagementPartner [[-PartnerId] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4bef8-105">설명</span><span class="sxs-lookup"><span data-stu-id="4bef8-105">DESCRIPTION</span></span>
<span data-ttu-id="4bef8-106">현재 인증된 사용자 또는 서비스 주체의 MPN(Microsoft 파트너 네트워크) ID를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="4bef8-106">Gets the Microsoft Partner Network(MPN) ID of the current authenticated user or service principal.</span></span>

## <span data-ttu-id="4bef8-107">예제</span><span class="sxs-lookup"><span data-stu-id="4bef8-107">EXAMPLES</span></span>

### <span data-ttu-id="4bef8-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="4bef8-108">Example 1</span></span>
```powershell
PS C:\> Get-AzManagementPartner
PartnerId   : 4977985
PartnerName : Test_Test_DPORTest
TenantId    : 1b1121dd-6900-412a-af73-e8d44f81e1c1
ObjectId    : aa67f786-0552-423e-8849-244ed12bf581
State       : Active
```

<span data-ttu-id="4bef8-109">현재 관리 파트너 ID를 얻게</span><span class="sxs-lookup"><span data-stu-id="4bef8-109">Get the current management partner id</span></span>

### <span data-ttu-id="4bef8-110">예제 2</span><span class="sxs-lookup"><span data-stu-id="4bef8-110">Example 2</span></span>
```powershell
PS C:\> Get-AzManagementPartner -PartnerId 4977985
PartnerId   : 4977985
PartnerName : Test_Test_DPORTest
TenantId    : 1b1121dd-6900-412a-af73-e8d44f81e1c1
ObjectId    : aa67f786-0552-423e-8849-244ed12bf581
State       : Active
```

<span data-ttu-id="4bef8-111">파트너 ID를 사용하여 현재 관리 파트너 ID를 얻게 됩니다. 일치하지 않는 경우 실패합니다.</span><span class="sxs-lookup"><span data-stu-id="4bef8-111">Get the current management partner id using a partner id, if they don't match, it will fail</span></span>

## <span data-ttu-id="4bef8-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4bef8-112">PARAMETERS</span></span>

### <span data-ttu-id="4bef8-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4bef8-113">-DefaultProfile</span></span>
<span data-ttu-id="4bef8-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="4bef8-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4bef8-115">-PartnerId</span><span class="sxs-lookup"><span data-stu-id="4bef8-115">-PartnerId</span></span>
<span data-ttu-id="4bef8-116">관리 파트너 ID로, 6자리 숫자입니다.</span><span class="sxs-lookup"><span data-stu-id="4bef8-116">The management partner id, it is a 6 digits number</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4bef8-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4bef8-117">CommonParameters</span></span>
<span data-ttu-id="4bef8-118">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="4bef8-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4bef8-119">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="4bef8-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4bef8-120">입력</span><span class="sxs-lookup"><span data-stu-id="4bef8-120">INPUTS</span></span>

### <span data-ttu-id="4bef8-121">없음</span><span class="sxs-lookup"><span data-stu-id="4bef8-121">None</span></span>

## <span data-ttu-id="4bef8-122">출력</span><span class="sxs-lookup"><span data-stu-id="4bef8-122">OUTPUTS</span></span>

### <span data-ttu-id="4bef8-123">Microsoft.Azure.Commands.ManagementPartner.PSManagementPartner</span><span class="sxs-lookup"><span data-stu-id="4bef8-123">Microsoft.Azure.Commands.ManagementPartner.PSManagementPartner</span></span>

## <span data-ttu-id="4bef8-124">참고 사항</span><span class="sxs-lookup"><span data-stu-id="4bef8-124">NOTES</span></span>

## <span data-ttu-id="4bef8-125">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4bef8-125">RELATED LINKS</span></span>

[<span data-ttu-id="4bef8-126">Remove-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="4bef8-126">Remove-AzManagementPartner</span></span>](./Remove-AzManagementPartner.md)

[<span data-ttu-id="4bef8-127">New-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="4bef8-127">New-AzManagementPartner</span></span>](./New-AzManagementPartner.md)

[<span data-ttu-id="4bef8-128">Update-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="4bef8-128">Update-AzManagementPartner</span></span>](./Update-AzManagementPartner.md)