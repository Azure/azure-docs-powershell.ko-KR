---
external help file: ''
Module Name: Az.VMWare
online version: https://docs.microsoft.com/powershell/module/az.vmware/get-azvmwareprivatecloudadmincredentials
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMware/help/Get-AzVMwarePrivateCloudAdminCredentials.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMware/help/Get-AzVMwarePrivateCloudAdminCredentials.md
ms.openlocfilehash: 88ecb5baff31ddcc27ce090f19a868c4d393c588
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101987168"
---
# <span data-ttu-id="c8d78-101">Get-AzVMWarePrivateCloudAdminCredentials</span><span class="sxs-lookup"><span data-stu-id="c8d78-101">Get-AzVMWarePrivateCloudAdminCredentials</span></span>

## <span data-ttu-id="c8d78-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c8d78-102">SYNOPSIS</span></span>
<span data-ttu-id="c8d78-103">사설 클라우드에 대한 관리자 자격 증명 나열</span><span class="sxs-lookup"><span data-stu-id="c8d78-103">List the admin credentials for the private cloud</span></span>

## <span data-ttu-id="c8d78-104">구문</span><span class="sxs-lookup"><span data-stu-id="c8d78-104">SYNTAX</span></span>

```
Get-AzVMWarePrivateCloudAdminCredentials -PrivateCloudName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="c8d78-105">설명</span><span class="sxs-lookup"><span data-stu-id="c8d78-105">DESCRIPTION</span></span>
<span data-ttu-id="c8d78-106">사설 클라우드에 대한 관리자 자격 증명 나열</span><span class="sxs-lookup"><span data-stu-id="c8d78-106">List the admin credentials for the private cloud</span></span>

## <span data-ttu-id="c8d78-107">예제</span><span class="sxs-lookup"><span data-stu-id="c8d78-107">EXAMPLES</span></span>

### <span data-ttu-id="c8d78-108">예제 1: 사설 클라우드의 관리자 자격 증명을 얻다</span><span class="sxs-lookup"><span data-stu-id="c8d78-108">Example 1: Get admin credential of private cloud</span></span>
```powershell
PS C:\> Get-AzVMWarePrivateCloudAdminCredentials -PrivateCloudName azps-test-cloud -ResourceGroupName azps-test-group

NsxtPassword NsxtUsername VcenterPassword VcenterUsername
------------ ------------ --------------- ---------------
************ admin        ************    cloudadmin@vsphere.local
```

<span data-ttu-id="c8d78-109">사설 클라우드의 관리자 자격 증명을 얻게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c8d78-109">Get admin credential of private cloud</span></span>

## <span data-ttu-id="c8d78-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="c8d78-110">PARAMETERS</span></span>

### <span data-ttu-id="c8d78-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c8d78-111">-DefaultProfile</span></span>
<span data-ttu-id="c8d78-112">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c8d78-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c8d78-113">-PrivateCloudName</span><span class="sxs-lookup"><span data-stu-id="c8d78-113">-PrivateCloudName</span></span>
<span data-ttu-id="c8d78-114">사설 클라우드의 이름</span><span class="sxs-lookup"><span data-stu-id="c8d78-114">Name of the private cloud</span></span>

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

### <span data-ttu-id="c8d78-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c8d78-115">-ResourceGroupName</span></span>
<span data-ttu-id="c8d78-116">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c8d78-116">The name of the resource group.</span></span>
<span data-ttu-id="c8d78-117">이름은 대소문자와 무관합니다.</span><span class="sxs-lookup"><span data-stu-id="c8d78-117">The name is case insensitive.</span></span>

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

### <span data-ttu-id="c8d78-118">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c8d78-118">-SubscriptionId</span></span>
<span data-ttu-id="c8d78-119">대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="c8d78-119">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="c8d78-120">-확인</span><span class="sxs-lookup"><span data-stu-id="c8d78-120">-Confirm</span></span>
<span data-ttu-id="c8d78-121">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="c8d78-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c8d78-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c8d78-122">-WhatIf</span></span>
<span data-ttu-id="c8d78-123">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="c8d78-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c8d78-124">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c8d78-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c8d78-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8d78-125">CommonParameters</span></span>
<span data-ttu-id="c8d78-126">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="c8d78-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8d78-127">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c8d78-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8d78-128">입력</span><span class="sxs-lookup"><span data-stu-id="c8d78-128">INPUTS</span></span>

## <span data-ttu-id="c8d78-129">출력</span><span class="sxs-lookup"><span data-stu-id="c8d78-129">OUTPUTS</span></span>

### <span data-ttu-id="c8d78-130">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.IAdminCredentials</span><span class="sxs-lookup"><span data-stu-id="c8d78-130">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.IAdminCredentials</span></span>

## <span data-ttu-id="c8d78-131">참고 사항</span><span class="sxs-lookup"><span data-stu-id="c8d78-131">NOTES</span></span>

<span data-ttu-id="c8d78-132">별칭</span><span class="sxs-lookup"><span data-stu-id="c8d78-132">ALIASES</span></span>

## <span data-ttu-id="c8d78-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c8d78-133">RELATED LINKS</span></span>

