---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ManagementPartner.dll-Help.xml
Module Name: Az.ManagementPartner
online version: https://docs.microsoft.com/en-us/powershell/module/az.managementpartner/get-azmanagementpartner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagementPartner/ManagementPartner/help/Get-AzManagementPartner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagementPartner/ManagementPartner/help/Get-AzManagementPartner.md
ms.openlocfilehash: 1031c9c8828969d16097953aa7440e2c8c0a8c1b
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93877705"
---
# <span data-ttu-id="903af-101">Get-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="903af-101">Get-AzManagementPartner</span></span>

## <span data-ttu-id="903af-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="903af-102">SYNOPSIS</span></span>
<span data-ttu-id="903af-103">현재 인증 된 사용자 또는 서비스 주체의 MPN (Microsoft 파트너 네트워크) ID를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="903af-103">Gets the Microsoft Partner Network(MPN) ID of the current authenticated user or service principal.</span></span>

## <span data-ttu-id="903af-104">구문과</span><span class="sxs-lookup"><span data-stu-id="903af-104">SYNTAX</span></span>

```
Get-AzManagementPartner [[-PartnerId] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="903af-105">설명은</span><span class="sxs-lookup"><span data-stu-id="903af-105">DESCRIPTION</span></span>
<span data-ttu-id="903af-106">현재 인증 된 사용자 또는 서비스 주체의 MPN (Microsoft 파트너 네트워크) ID를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="903af-106">Gets the Microsoft Partner Network(MPN) ID of the current authenticated user or service principal.</span></span>

## <span data-ttu-id="903af-107">예제의</span><span class="sxs-lookup"><span data-stu-id="903af-107">EXAMPLES</span></span>

### <span data-ttu-id="903af-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="903af-108">Example 1</span></span>
```powershell
PS C:\> Get-AzManagementPartner
PartnerId   : 4977985
PartnerName : Test_Test_DPORTest
TenantId    : 1b1121dd-6900-412a-af73-e8d44f81e1c1
ObjectId    : aa67f786-0552-423e-8849-244ed12bf581
State       : Active
```

<span data-ttu-id="903af-109">현재 관리 파트너 id 가져오기</span><span class="sxs-lookup"><span data-stu-id="903af-109">Get the current management partner id</span></span>

### <span data-ttu-id="903af-110">예제 2</span><span class="sxs-lookup"><span data-stu-id="903af-110">Example 2</span></span>
```powershell
PS C:\> Get-AzManagementPartner -PartnerId 4977985
PartnerId   : 4977985
PartnerName : Test_Test_DPORTest
TenantId    : 1b1121dd-6900-412a-af73-e8d44f81e1c1
ObjectId    : aa67f786-0552-423e-8849-244ed12bf581
State       : Active
```

<span data-ttu-id="903af-111">파트너 id를 사용 하 여 현재 관리 파트너 id 가져오기 일치 하지 않으면 실패 합니다.</span><span class="sxs-lookup"><span data-stu-id="903af-111">Get the current management partner id using a partner id, if they don't match, it will fail</span></span>

## <span data-ttu-id="903af-112">변수</span><span class="sxs-lookup"><span data-stu-id="903af-112">PARAMETERS</span></span>

### <span data-ttu-id="903af-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="903af-113">-DefaultProfile</span></span>
<span data-ttu-id="903af-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="903af-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="903af-115">-(또는)-(Id)</span><span class="sxs-lookup"><span data-stu-id="903af-115">-PartnerId</span></span>
<span data-ttu-id="903af-116">관리 파트너 id로 6 자리 숫자입니다.</span><span class="sxs-lookup"><span data-stu-id="903af-116">The management partner id, it is a 6 digits number</span></span>

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

### <span data-ttu-id="903af-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="903af-117">CommonParameters</span></span>
<span data-ttu-id="903af-118">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="903af-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="903af-119">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="903af-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="903af-120">입력</span><span class="sxs-lookup"><span data-stu-id="903af-120">INPUTS</span></span>

### <span data-ttu-id="903af-121">않아야</span><span class="sxs-lookup"><span data-stu-id="903af-121">None</span></span>

## <span data-ttu-id="903af-122">출력</span><span class="sxs-lookup"><span data-stu-id="903af-122">OUTPUTS</span></span>

### <span data-ttu-id="903af-123">Microsoft Azure. PSManagementPartner</span><span class="sxs-lookup"><span data-stu-id="903af-123">Microsoft.Azure.Commands.ManagementPartner.PSManagementPartner</span></span>

## <span data-ttu-id="903af-124">상속자</span><span class="sxs-lookup"><span data-stu-id="903af-124">NOTES</span></span>

## <span data-ttu-id="903af-125">관련 링크</span><span class="sxs-lookup"><span data-stu-id="903af-125">RELATED LINKS</span></span>

[<span data-ttu-id="903af-126">제거-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="903af-126">Remove-AzManagementPartner</span></span>](./Remove-AzManagementPartner.md)

[<span data-ttu-id="903af-127">새로운 AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="903af-127">New-AzManagementPartner</span></span>](./New-AzManagementPartner.md)

[<span data-ttu-id="903af-128">업데이트-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="903af-128">Update-AzManagementPartner</span></span>](./Update-AzManagementPartner.md)