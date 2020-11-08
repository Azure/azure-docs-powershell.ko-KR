---
external help file: ''
Module Name: Az.VMWare
online version: https://docs.microsoft.com/en-us/powershell/module/az.vmware/get-azvmwareprivatecloudadmincredentials
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/Get-AzVMWarePrivateCloudAdminCredentials.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/Get-AzVMWarePrivateCloudAdminCredentials.md
ms.openlocfilehash: 64552dada33249779e474dc72063f828c9336ffd
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94056034"
---
# <span data-ttu-id="33fe5-101">Get-AzVMWarePrivateCloudAdminCredentials</span><span class="sxs-lookup"><span data-stu-id="33fe5-101">Get-AzVMWarePrivateCloudAdminCredentials</span></span>

## <span data-ttu-id="33fe5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="33fe5-102">SYNOPSIS</span></span>
<span data-ttu-id="33fe5-103">사설 클라우드의 관리자 자격 증명 나열</span><span class="sxs-lookup"><span data-stu-id="33fe5-103">List the admin credentials for the private cloud</span></span>

## <span data-ttu-id="33fe5-104">구문과</span><span class="sxs-lookup"><span data-stu-id="33fe5-104">SYNTAX</span></span>

```
Get-AzVMWarePrivateCloudAdminCredentials -PrivateCloudName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="33fe5-105">설명은</span><span class="sxs-lookup"><span data-stu-id="33fe5-105">DESCRIPTION</span></span>
<span data-ttu-id="33fe5-106">사설 클라우드의 관리자 자격 증명 나열</span><span class="sxs-lookup"><span data-stu-id="33fe5-106">List the admin credentials for the private cloud</span></span>

## <span data-ttu-id="33fe5-107">예제의</span><span class="sxs-lookup"><span data-stu-id="33fe5-107">EXAMPLES</span></span>

### <span data-ttu-id="33fe5-108">예제 1: 사설 클라우드의 관리자 자격 증명 가져오기</span><span class="sxs-lookup"><span data-stu-id="33fe5-108">Example 1: Get admin credential of private cloud</span></span>
```powershell
PS C:\> Get-AzVMWarePrivateCloudAdminCredentials -PrivateCloudName azps-test-cloud -ResourceGroupName azps-test-group

NsxtPassword NsxtUsername VcenterPassword VcenterUsername
------------ ------------ --------------- ---------------
************ admin        ************    cloudadmin@vsphere.local
```

<span data-ttu-id="33fe5-109">사설 클라우드의 관리자 자격 증명 가져오기</span><span class="sxs-lookup"><span data-stu-id="33fe5-109">Get admin credential of private cloud</span></span>

## <span data-ttu-id="33fe5-110">변수</span><span class="sxs-lookup"><span data-stu-id="33fe5-110">PARAMETERS</span></span>

### <span data-ttu-id="33fe5-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="33fe5-111">-DefaultProfile</span></span>
<span data-ttu-id="33fe5-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="33fe5-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33fe5-113">-PrivateCloudName</span><span class="sxs-lookup"><span data-stu-id="33fe5-113">-PrivateCloudName</span></span>
<span data-ttu-id="33fe5-114">사설 클라우드의 이름</span><span class="sxs-lookup"><span data-stu-id="33fe5-114">Name of the private cloud</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33fe5-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="33fe5-115">-ResourceGroupName</span></span>
<span data-ttu-id="33fe5-116">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="33fe5-116">The name of the resource group.</span></span>
<span data-ttu-id="33fe5-117">이름은 대/소문자를 구분 합니다.</span><span class="sxs-lookup"><span data-stu-id="33fe5-117">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33fe5-118">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="33fe5-118">-SubscriptionId</span></span>
<span data-ttu-id="33fe5-119">대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="33fe5-119">The ID of the target subscription.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33fe5-120">-확인</span><span class="sxs-lookup"><span data-stu-id="33fe5-120">-Confirm</span></span>
<span data-ttu-id="33fe5-121">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="33fe5-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="33fe5-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="33fe5-122">-WhatIf</span></span>
<span data-ttu-id="33fe5-123">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="33fe5-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="33fe5-124">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="33fe5-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="33fe5-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="33fe5-125">CommonParameters</span></span>
<span data-ttu-id="33fe5-126">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="33fe5-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="33fe5-127">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="33fe5-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="33fe5-128">입력</span><span class="sxs-lookup"><span data-stu-id="33fe5-128">INPUTS</span></span>

## <span data-ttu-id="33fe5-129">출력</span><span class="sxs-lookup"><span data-stu-id="33fe5-129">OUTPUTS</span></span>

### <span data-ttu-id="33fe5-130">Api20200320. IAdminCredentials 증명으로 제공 됩니다.</span><span class="sxs-lookup"><span data-stu-id="33fe5-130">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.IAdminCredentials</span></span>

## <span data-ttu-id="33fe5-131">상속자</span><span class="sxs-lookup"><span data-stu-id="33fe5-131">NOTES</span></span>

<span data-ttu-id="33fe5-132">별칭과</span><span class="sxs-lookup"><span data-stu-id="33fe5-132">ALIASES</span></span>

## <span data-ttu-id="33fe5-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="33fe5-133">RELATED LINKS</span></span>

