---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ManagementPartner.dll-Help.xml
Module Name: Az.ManagementPartner
online version: https://docs.microsoft.com/powershell/module/az.managementpartner/get-azmanagementpartner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagementPartner/ManagementPartner/help/Get-AzManagementPartner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagementPartner/ManagementPartner/help/Get-AzManagementPartner.md
ms.openlocfilehash: e09e63ed68ac87156fd03f73c992043b8a0271cf
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101983083"
---
# <span data-ttu-id="1ecb5-101">Get-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="1ecb5-101">Get-AzManagementPartner</span></span>

## <span data-ttu-id="1ecb5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1ecb5-102">SYNOPSIS</span></span>
<span data-ttu-id="1ecb5-103">현재 인증된 사용자 또는 서비스 주체의 MPN(Microsoft 파트너 네트워크) ID를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="1ecb5-103">Gets the Microsoft Partner Network(MPN) ID of the current authenticated user or service principal.</span></span>

## <span data-ttu-id="1ecb5-104">구문</span><span class="sxs-lookup"><span data-stu-id="1ecb5-104">SYNTAX</span></span>

```
Get-AzManagementPartner [[-PartnerId] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1ecb5-105">설명</span><span class="sxs-lookup"><span data-stu-id="1ecb5-105">DESCRIPTION</span></span>
<span data-ttu-id="1ecb5-106">현재 인증된 사용자 또는 서비스 주체의 MPN(Microsoft 파트너 네트워크) ID를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="1ecb5-106">Gets the Microsoft Partner Network(MPN) ID of the current authenticated user or service principal.</span></span>

## <span data-ttu-id="1ecb5-107">예제</span><span class="sxs-lookup"><span data-stu-id="1ecb5-107">EXAMPLES</span></span>

### <span data-ttu-id="1ecb5-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="1ecb5-108">Example 1</span></span>
```powershell
PS C:\> Get-AzManagementPartner
PartnerId   : 4977985
PartnerName : Test_Test_DPORTest
TenantId    : 1b1121dd-6900-412a-af73-e8d44f81e1c1
ObjectId    : aa67f786-0552-423e-8849-244ed12bf581
State       : Active
```

<span data-ttu-id="1ecb5-109">현재 관리 파트너 ID를 얻다</span><span class="sxs-lookup"><span data-stu-id="1ecb5-109">Get the current management partner id</span></span>

### <span data-ttu-id="1ecb5-110">예제 2</span><span class="sxs-lookup"><span data-stu-id="1ecb5-110">Example 2</span></span>
```powershell
PS C:\> Get-AzManagementPartner -PartnerId 4977985
PartnerId   : 4977985
PartnerName : Test_Test_DPORTest
TenantId    : 1b1121dd-6900-412a-af73-e8d44f81e1c1
ObjectId    : aa67f786-0552-423e-8849-244ed12bf581
State       : Active
```

<span data-ttu-id="1ecb5-111">파트너 ID를 사용하여 현재 관리 파트너 ID를 얻지 못하면 실패합니다.</span><span class="sxs-lookup"><span data-stu-id="1ecb5-111">Get the current management partner id using a partner id, if they don't match, it will fail</span></span>

## <span data-ttu-id="1ecb5-112">매개 변수</span><span class="sxs-lookup"><span data-stu-id="1ecb5-112">PARAMETERS</span></span>

### <span data-ttu-id="1ecb5-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1ecb5-113">-DefaultProfile</span></span>
<span data-ttu-id="1ecb5-114">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="1ecb5-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1ecb5-115">-PartnerId</span><span class="sxs-lookup"><span data-stu-id="1ecb5-115">-PartnerId</span></span>
<span data-ttu-id="1ecb5-116">관리 파트너 ID는 6자리 숫자입니다.</span><span class="sxs-lookup"><span data-stu-id="1ecb5-116">The management partner id, it is a 6 digits number</span></span>

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

### <span data-ttu-id="1ecb5-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ecb5-117">CommonParameters</span></span>
<span data-ttu-id="1ecb5-118">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="1ecb5-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ecb5-119">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="1ecb5-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ecb5-120">입력</span><span class="sxs-lookup"><span data-stu-id="1ecb5-120">INPUTS</span></span>

### <span data-ttu-id="1ecb5-121">없음</span><span class="sxs-lookup"><span data-stu-id="1ecb5-121">None</span></span>

## <span data-ttu-id="1ecb5-122">출력</span><span class="sxs-lookup"><span data-stu-id="1ecb5-122">OUTPUTS</span></span>

### <span data-ttu-id="1ecb5-123">Microsoft.Azure.Commands.ManagementPartner.PSManagementPartner</span><span class="sxs-lookup"><span data-stu-id="1ecb5-123">Microsoft.Azure.Commands.ManagementPartner.PSManagementPartner</span></span>

## <span data-ttu-id="1ecb5-124">참고 사항</span><span class="sxs-lookup"><span data-stu-id="1ecb5-124">NOTES</span></span>

## <span data-ttu-id="1ecb5-125">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1ecb5-125">RELATED LINKS</span></span>

[<span data-ttu-id="1ecb5-126">Remove-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="1ecb5-126">Remove-AzManagementPartner</span></span>](./Remove-AzManagementPartner.md)

[<span data-ttu-id="1ecb5-127">New-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="1ecb5-127">New-AzManagementPartner</span></span>](./New-AzManagementPartner.md)

[<span data-ttu-id="1ecb5-128">Update-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="1ecb5-128">Update-AzManagementPartner</span></span>](./Update-AzManagementPartner.md)