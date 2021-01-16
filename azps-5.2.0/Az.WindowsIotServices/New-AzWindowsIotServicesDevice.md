---
external help file: ''
Module Name: Az.WindowsIotServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.windowsiotservices/new-azwindowsiotservicesdevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/WindowsIotServices/help/New-AzWindowsIotServicesDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/WindowsIotServices/help/New-AzWindowsIotServicesDevice.md
ms.openlocfilehash: 4da60a6d4083992f843121cb141a453b4ef3b4b8
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98347282"
---
# <span data-ttu-id="28d0c-101">New-AzWindowsIotServicesDevice</span><span class="sxs-lookup"><span data-stu-id="28d0c-101">New-AzWindowsIotServicesDevice</span></span>

## <span data-ttu-id="28d0c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="28d0c-102">SYNOPSIS</span></span>
<span data-ttu-id="28d0c-103">Windows IoT 디바이스 서비스의 메타데이터를 만들거나 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="28d0c-103">Create or update the metadata of a Windows IoT Device Service.</span></span>
<span data-ttu-id="28d0c-104">속성을 수정하는 일반적인 패턴은 Windows IoT 디바이스 서비스 메타데이터 및 보안 메타데이터를 검색한 다음 새 본문의 수정된 값과 결합하여 Windows IoT Device Service를 업데이트하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="28d0c-104">The usual pattern to modify a property is to retrieve the Windows IoT Device Service metadata and security metadata, and then combine them with the modified values in a new body to update the Windows IoT Device Service.</span></span>

## <span data-ttu-id="28d0c-105">구문</span><span class="sxs-lookup"><span data-stu-id="28d0c-105">SYNTAX</span></span>

```
New-AzWindowsIotServicesDevice -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-IfMatch <String>] [-AdminDomainName <String>] [-BillingDomainName <String>] [-Etag <String>]
 [-Location <String>] [-Note <String>] [-Quantity <Int64>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="28d0c-106">설명</span><span class="sxs-lookup"><span data-stu-id="28d0c-106">DESCRIPTION</span></span>
<span data-ttu-id="28d0c-107">Windows IoT 디바이스 서비스의 메타데이터를 만들거나 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="28d0c-107">Create or update the metadata of a Windows IoT Device Service.</span></span>
<span data-ttu-id="28d0c-108">속성을 수정하는 일반적인 패턴은 Windows IoT 디바이스 서비스 메타데이터 및 보안 메타데이터를 검색한 다음 새 본문의 수정된 값과 결합하여 Windows IoT Device Service를 업데이트하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="28d0c-108">The usual pattern to modify a property is to retrieve the Windows IoT Device Service metadata and security metadata, and then combine them with the modified values in a new body to update the Windows IoT Device Service.</span></span>

## <span data-ttu-id="28d0c-109">예제</span><span class="sxs-lookup"><span data-stu-id="28d0c-109">EXAMPLES</span></span>

### <span data-ttu-id="28d0c-110">예제 1: 새 Windows IoT 서비스 만들기</span><span class="sxs-lookup"><span data-stu-id="28d0c-110">Example 1: Create a new Windows IoT services</span></span>
```powershell
PS C:\> New-AzWindowsIotServicesDevice -Name wsi-t03 -ResourceGroupName azure-rg-test -Location eastus -Quantity 10 -BillingDomainName 'microsoft.onmicrosoft.com' -AdminDomainName 'microsoft.onmicrosoft.com'

Location Name    Type                                Etag
-------- ----    ----                                ----
eastus   wsi-t03 Microsoft.WindowsIoT/DeviceServices "6a00eee9-0000-0700-0000-5fab82870000"
```

<span data-ttu-id="28d0c-111">이 명령은 새 Windows IoT 서비스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="28d0c-111">This command creates a new Windows IoT services.</span></span>

## <span data-ttu-id="28d0c-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="28d0c-112">PARAMETERS</span></span>

### <span data-ttu-id="28d0c-113">-AdminDomainName</span><span class="sxs-lookup"><span data-stu-id="28d0c-113">-AdminDomainName</span></span>
<span data-ttu-id="28d0c-114">Windows IoT Device Service OEM AAD 도메인</span><span class="sxs-lookup"><span data-stu-id="28d0c-114">Windows IoT Device Service OEM AAD domain</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28d0c-115">-BillingDomainName</span><span class="sxs-lookup"><span data-stu-id="28d0c-115">-BillingDomainName</span></span>
<span data-ttu-id="28d0c-116">Windows IoT Device Service ODM AAD 도메인</span><span class="sxs-lookup"><span data-stu-id="28d0c-116">Windows IoT Device Service ODM AAD domain</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28d0c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="28d0c-117">-DefaultProfile</span></span>
<span data-ttu-id="28d0c-118">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="28d0c-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="28d0c-119">-Etag</span><span class="sxs-lookup"><span data-stu-id="28d0c-119">-Etag</span></span>
<span data-ttu-id="28d0c-120">Etag 필드는 *필요하지* 않습니다.</span><span class="sxs-lookup"><span data-stu-id="28d0c-120">The Etag field is *not* required.</span></span>
<span data-ttu-id="28d0c-121">응답 본문에 제공된 경우 일반 ETag 규칙에 따라 헤더로 제공되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="28d0c-121">If it is provided in the response body, it must also be provided as a header per the normal ETag convention.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28d0c-122">-IfMatch</span><span class="sxs-lookup"><span data-stu-id="28d0c-122">-IfMatch</span></span>
<span data-ttu-id="28d0c-123">Windows IoT 디바이스 서비스의 ETag입니다.</span><span class="sxs-lookup"><span data-stu-id="28d0c-123">ETag of the Windows IoT Device Service.</span></span>
<span data-ttu-id="28d0c-124">새 Windows IoT 디바이스 서비스를 만들기 위해 지정하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="28d0c-124">Do not specify for creating a new Windows IoT Device Service.</span></span>
<span data-ttu-id="28d0c-125">기존 Windows IoT 디바이스 서비스를 업데이트하는 데 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="28d0c-125">Required to update an existing Windows IoT Device Service.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28d0c-126">-Location</span><span class="sxs-lookup"><span data-stu-id="28d0c-126">-Location</span></span>
<span data-ttu-id="28d0c-127">리소스가 있는 Azure 지역</span><span class="sxs-lookup"><span data-stu-id="28d0c-127">The Azure Region where the resource lives</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28d0c-128">-Name</span><span class="sxs-lookup"><span data-stu-id="28d0c-128">-Name</span></span>
<span data-ttu-id="28d0c-129">Windows IoT 디바이스 서비스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="28d0c-129">The name of the Windows IoT Device Service.</span></span>

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

### <span data-ttu-id="28d0c-130">-Note</span><span class="sxs-lookup"><span data-stu-id="28d0c-130">-Note</span></span>
<span data-ttu-id="28d0c-131">Windows IoT 디바이스 서비스 정보.</span><span class="sxs-lookup"><span data-stu-id="28d0c-131">Windows IoT Device Service notes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28d0c-132">-Quantity</span><span class="sxs-lookup"><span data-stu-id="28d0c-132">-Quantity</span></span>
<span data-ttu-id="28d0c-133">Windows IoT Device Service 디바이스 할당,</span><span class="sxs-lookup"><span data-stu-id="28d0c-133">Windows IoT Device Service device allocation,</span></span>

```yaml
Type: System.Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28d0c-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="28d0c-134">-ResourceGroupName</span></span>
<span data-ttu-id="28d0c-135">Windows IoT Device Service를 포함하는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="28d0c-135">The name of the resource group that contains the Windows IoT Device Service.</span></span>

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

### <span data-ttu-id="28d0c-136">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="28d0c-136">-SubscriptionId</span></span>
<span data-ttu-id="28d0c-137">구독 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="28d0c-137">The subscription identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28d0c-138">-Tag</span><span class="sxs-lookup"><span data-stu-id="28d0c-138">-Tag</span></span>
<span data-ttu-id="28d0c-139">리소스 태그.</span><span class="sxs-lookup"><span data-stu-id="28d0c-139">Resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28d0c-140">-Confirm</span><span class="sxs-lookup"><span data-stu-id="28d0c-140">-Confirm</span></span>
<span data-ttu-id="28d0c-141">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="28d0c-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="28d0c-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="28d0c-142">-WhatIf</span></span>
<span data-ttu-id="28d0c-143">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="28d0c-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="28d0c-144">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="28d0c-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="28d0c-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28d0c-145">CommonParameters</span></span>
<span data-ttu-id="28d0c-146">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="28d0c-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="28d0c-147">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="28d0c-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28d0c-148">입력</span><span class="sxs-lookup"><span data-stu-id="28d0c-148">INPUTS</span></span>

## <span data-ttu-id="28d0c-149">출력</span><span class="sxs-lookup"><span data-stu-id="28d0c-149">OUTPUTS</span></span>

### <span data-ttu-id="28d0c-150">Microsoft.Azure.PowerShell.Cmdlets.WindowsIotServices.Models.Api20190601.IDeviceService</span><span class="sxs-lookup"><span data-stu-id="28d0c-150">Microsoft.Azure.PowerShell.Cmdlets.WindowsIotServices.Models.Api20190601.IDeviceService</span></span>

## <span data-ttu-id="28d0c-151">참고 사항</span><span class="sxs-lookup"><span data-stu-id="28d0c-151">NOTES</span></span>

<span data-ttu-id="28d0c-152">별칭</span><span class="sxs-lookup"><span data-stu-id="28d0c-152">ALIASES</span></span>

## <span data-ttu-id="28d0c-153">관련 링크</span><span class="sxs-lookup"><span data-stu-id="28d0c-153">RELATED LINKS</span></span>

