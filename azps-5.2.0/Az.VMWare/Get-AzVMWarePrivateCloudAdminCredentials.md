---
external help file: ''
Module Name: Az.VMWare
online version: https://docs.microsoft.com/en-us/powershell/module/az.vmware/get-azvmwareprivatecloudadmincredentials
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/Get-AzVMWarePrivateCloudAdminCredentials.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/Get-AzVMWarePrivateCloudAdminCredentials.md
ms.openlocfilehash: 64552dada33249779e474dc72063f828c9336ffd
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98325751"
---
# <span data-ttu-id="38fee-101">Get-AzVMWarePrivateCloudAdminCredentials</span><span class="sxs-lookup"><span data-stu-id="38fee-101">Get-AzVMWarePrivateCloudAdminCredentials</span></span>

## <span data-ttu-id="38fee-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="38fee-102">SYNOPSIS</span></span>
<span data-ttu-id="38fee-103">사설 클라우드에 대한 관리자 자격 증명 나열</span><span class="sxs-lookup"><span data-stu-id="38fee-103">List the admin credentials for the private cloud</span></span>

## <span data-ttu-id="38fee-104">구문</span><span class="sxs-lookup"><span data-stu-id="38fee-104">SYNTAX</span></span>

```
Get-AzVMWarePrivateCloudAdminCredentials -PrivateCloudName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="38fee-105">설명</span><span class="sxs-lookup"><span data-stu-id="38fee-105">DESCRIPTION</span></span>
<span data-ttu-id="38fee-106">사설 클라우드에 대한 관리자 자격 증명 나열</span><span class="sxs-lookup"><span data-stu-id="38fee-106">List the admin credentials for the private cloud</span></span>

## <span data-ttu-id="38fee-107">예제</span><span class="sxs-lookup"><span data-stu-id="38fee-107">EXAMPLES</span></span>

### <span data-ttu-id="38fee-108">예제 1: 사설 클라우드의 관리자 자격 증명을 얻게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="38fee-108">Example 1: Get admin credential of private cloud</span></span>
```powershell
PS C:\> Get-AzVMWarePrivateCloudAdminCredentials -PrivateCloudName azps-test-cloud -ResourceGroupName azps-test-group

NsxtPassword NsxtUsername VcenterPassword VcenterUsername
------------ ------------ --------------- ---------------
************ admin        ************    cloudadmin@vsphere.local
```

<span data-ttu-id="38fee-109">사설 클라우드의 관리자 자격 증명을 얻게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="38fee-109">Get admin credential of private cloud</span></span>

## <span data-ttu-id="38fee-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="38fee-110">PARAMETERS</span></span>

### <span data-ttu-id="38fee-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="38fee-111">-DefaultProfile</span></span>
<span data-ttu-id="38fee-112">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="38fee-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="38fee-113">-PrivateCloudName</span><span class="sxs-lookup"><span data-stu-id="38fee-113">-PrivateCloudName</span></span>
<span data-ttu-id="38fee-114">사설 클라우드의 이름</span><span class="sxs-lookup"><span data-stu-id="38fee-114">Name of the private cloud</span></span>

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

### <span data-ttu-id="38fee-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="38fee-115">-ResourceGroupName</span></span>
<span data-ttu-id="38fee-116">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="38fee-116">The name of the resource group.</span></span>
<span data-ttu-id="38fee-117">이름은 대소문자 무관합니다.</span><span class="sxs-lookup"><span data-stu-id="38fee-117">The name is case insensitive.</span></span>

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

### <span data-ttu-id="38fee-118">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="38fee-118">-SubscriptionId</span></span>
<span data-ttu-id="38fee-119">대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="38fee-119">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="38fee-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="38fee-120">-Confirm</span></span>
<span data-ttu-id="38fee-121">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="38fee-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="38fee-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="38fee-122">-WhatIf</span></span>
<span data-ttu-id="38fee-123">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="38fee-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="38fee-124">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="38fee-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="38fee-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38fee-125">CommonParameters</span></span>
<span data-ttu-id="38fee-126">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="38fee-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38fee-127">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="38fee-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38fee-128">입력</span><span class="sxs-lookup"><span data-stu-id="38fee-128">INPUTS</span></span>

## <span data-ttu-id="38fee-129">출력</span><span class="sxs-lookup"><span data-stu-id="38fee-129">OUTPUTS</span></span>

### <span data-ttu-id="38fee-130">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.IAdminCredentials</span><span class="sxs-lookup"><span data-stu-id="38fee-130">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.IAdminCredentials</span></span>

## <span data-ttu-id="38fee-131">참고 사항</span><span class="sxs-lookup"><span data-stu-id="38fee-131">NOTES</span></span>

<span data-ttu-id="38fee-132">별칭</span><span class="sxs-lookup"><span data-stu-id="38fee-132">ALIASES</span></span>

## <span data-ttu-id="38fee-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="38fee-133">RELATED LINKS</span></span>

