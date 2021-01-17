---
external help file: ''
Module Name: Az.WindowsIotServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.windowsiotservices/update-azwindowsiotservicesdevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/WindowsIotServices/help/Update-AzWindowsIotServicesDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/WindowsIotServices/help/Update-AzWindowsIotServicesDevice.md
ms.openlocfilehash: 5e50ad3dc1ce2396dfb7a2b498efc82c4e95e430
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98371463"
---
# <span data-ttu-id="37dbc-101">Update-AzWindowsIotServicesDevice</span><span class="sxs-lookup"><span data-stu-id="37dbc-101">Update-AzWindowsIotServicesDevice</span></span>

## <span data-ttu-id="37dbc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="37dbc-102">SYNOPSIS</span></span>
<span data-ttu-id="37dbc-103">Windows IoT 디바이스 서비스의 메타데이터를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="37dbc-103">Updates the metadata of a Windows IoT Device Service.</span></span>
<span data-ttu-id="37dbc-104">속성을 수정하는 일반적인 패턴은 Windows IoT 디바이스 서비스 메타데이터 및 보안 메타데이터를 검색한 다음 새 본문의 수정된 값과 결합하여 Windows IoT Device Service를 업데이트하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="37dbc-104">The usual pattern to modify a property is to retrieve the Windows IoT Device Service metadata and security metadata, and then combine them with the modified values in a new body to update the Windows IoT Device Service.</span></span>

## <span data-ttu-id="37dbc-105">구문</span><span class="sxs-lookup"><span data-stu-id="37dbc-105">SYNTAX</span></span>

### <span data-ttu-id="37dbc-106">UpdateExpanded(기본값)</span><span class="sxs-lookup"><span data-stu-id="37dbc-106">UpdateExpanded (Default)</span></span>
```
Update-AzWindowsIotServicesDevice -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-IfMatch <String>] [-AdminDomainName <String>] [-BillingDomainName <String>] [-Etag <String>]
 [-Location <String>] [-Note <String>] [-Quantity <Int64>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="37dbc-107">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="37dbc-107">UpdateViaIdentityExpanded</span></span>
```
Update-AzWindowsIotServicesDevice -InputObject <IWindowsIotServicesIdentity> [-IfMatch <String>]
 [-AdminDomainName <String>] [-BillingDomainName <String>] [-Etag <String>] [-Location <String>]
 [-Note <String>] [-Quantity <Int64>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="37dbc-108">설명</span><span class="sxs-lookup"><span data-stu-id="37dbc-108">DESCRIPTION</span></span>
<span data-ttu-id="37dbc-109">Windows IoT 디바이스 서비스의 메타데이터를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="37dbc-109">Updates the metadata of a Windows IoT Device Service.</span></span>
<span data-ttu-id="37dbc-110">속성을 수정하는 일반적인 패턴은 Windows IoT 디바이스 서비스 메타데이터 및 보안 메타데이터를 검색한 다음 새 본문의 수정된 값과 결합하여 Windows IoT Device Service를 업데이트하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="37dbc-110">The usual pattern to modify a property is to retrieve the Windows IoT Device Service metadata and security metadata, and then combine them with the modified values in a new body to update the Windows IoT Device Service.</span></span>

## <span data-ttu-id="37dbc-111">예제</span><span class="sxs-lookup"><span data-stu-id="37dbc-111">EXAMPLES</span></span>

### <span data-ttu-id="37dbc-112">예제 1: 이름으로 Windows IoT 서비스 업데이트</span><span class="sxs-lookup"><span data-stu-id="37dbc-112">Example 1: Update a Windows IoT services by name</span></span>
```powershell
PS C:\> Update-AzWindowsIotServicesDevice -Name wsi-t03 -ResourceGroupName azure-rg-test -Quantity 10

Location Name    Type                                Etag
-------- ----    ----                                ----
eastus   wsi-t03 Microsoft.WindowsIoT/DeviceServices "5d006a5c-0000-0700-0000-5faa46760000"
```

<span data-ttu-id="37dbc-113">이 명령은 이름으로 Windows IoT 서비스를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="37dbc-113">This command updates a Windows IoT services by name.</span></span>

### <span data-ttu-id="37dbc-114">예제 2: 파이프라인으로 Windows IoT 서비스 업데이트</span><span class="sxs-lookup"><span data-stu-id="37dbc-114">Example 2: Update a Windows IoT services by pipeline</span></span>
```powershell
PS C:\> Get-AzWindowsIotServicesDevice -Name wsi-t03 -ResourceGroupName azure-rg-test | Update-AzWindowsIotServicesDevice-Quantity 100 -Tag @{'oper'='update'}

Location Name    Type                                Etag
-------- ----    ----                                ----
West US  wsi-t01 Microsoft.WindowsIoT/DeviceServices "5d005f5f-0000-0700-0000-5faa46ae0000"
```

<span data-ttu-id="37dbc-115">이 명령은 파이프라인에 의해 Windows IoT 서비스를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="37dbc-115">This command updates a Windows IoT services by pipeline.</span></span>

## <span data-ttu-id="37dbc-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="37dbc-116">PARAMETERS</span></span>

### <span data-ttu-id="37dbc-117">-AdminDomainName</span><span class="sxs-lookup"><span data-stu-id="37dbc-117">-AdminDomainName</span></span>
<span data-ttu-id="37dbc-118">Windows IoT Device Service OEM AAD 도메인</span><span class="sxs-lookup"><span data-stu-id="37dbc-118">Windows IoT Device Service OEM AAD domain</span></span>

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

### <span data-ttu-id="37dbc-119">-BillingDomainName</span><span class="sxs-lookup"><span data-stu-id="37dbc-119">-BillingDomainName</span></span>
<span data-ttu-id="37dbc-120">Windows IoT Device Service ODM AAD 도메인</span><span class="sxs-lookup"><span data-stu-id="37dbc-120">Windows IoT Device Service ODM AAD domain</span></span>

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

### <span data-ttu-id="37dbc-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="37dbc-121">-DefaultProfile</span></span>
<span data-ttu-id="37dbc-122">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="37dbc-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="37dbc-123">-Etag</span><span class="sxs-lookup"><span data-stu-id="37dbc-123">-Etag</span></span>
<span data-ttu-id="37dbc-124">Etag 필드는 *필요하지* 않습니다.</span><span class="sxs-lookup"><span data-stu-id="37dbc-124">The Etag field is *not* required.</span></span>
<span data-ttu-id="37dbc-125">응답 본문에 제공된 경우 일반 ETag 규칙에 따라 헤더로 제공되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="37dbc-125">If it is provided in the response body, it must also be provided as a header per the normal ETag convention.</span></span>

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

### <span data-ttu-id="37dbc-126">-IfMatch</span><span class="sxs-lookup"><span data-stu-id="37dbc-126">-IfMatch</span></span>
<span data-ttu-id="37dbc-127">Windows IoT 디바이스 서비스의 ETag입니다.</span><span class="sxs-lookup"><span data-stu-id="37dbc-127">ETag of the Windows IoT Device Service.</span></span>
<span data-ttu-id="37dbc-128">새로운 Windows IoT Device Service를 만들기 위해 지정하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="37dbc-128">Do not specify for creating a brand new Windows IoT Device Service.</span></span>
<span data-ttu-id="37dbc-129">기존 Windows IoT 디바이스 서비스를 업데이트하는 데 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="37dbc-129">Required to update an existing Windows IoT Device Service.</span></span>

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

### <span data-ttu-id="37dbc-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="37dbc-130">-InputObject</span></span>
<span data-ttu-id="37dbc-131">ID 매개 변수를 생성하는 경우 INPUTOBJECT 속성에 대한 NOTES 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="37dbc-131">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.WindowsIotServices.Models.IWindowsIotServicesIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="37dbc-132">-Location</span><span class="sxs-lookup"><span data-stu-id="37dbc-132">-Location</span></span>
<span data-ttu-id="37dbc-133">리소스가 있는 Azure 지역</span><span class="sxs-lookup"><span data-stu-id="37dbc-133">The Azure Region where the resource lives</span></span>

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

### <span data-ttu-id="37dbc-134">-Name</span><span class="sxs-lookup"><span data-stu-id="37dbc-134">-Name</span></span>
<span data-ttu-id="37dbc-135">Windows IoT 디바이스 서비스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="37dbc-135">The name of the Windows IoT Device Service.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37dbc-136">-Note</span><span class="sxs-lookup"><span data-stu-id="37dbc-136">-Note</span></span>
<span data-ttu-id="37dbc-137">Windows IoT 디바이스 서비스 정보.</span><span class="sxs-lookup"><span data-stu-id="37dbc-137">Windows IoT Device Service notes.</span></span>

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

### <span data-ttu-id="37dbc-138">-Quantity</span><span class="sxs-lookup"><span data-stu-id="37dbc-138">-Quantity</span></span>
<span data-ttu-id="37dbc-139">Windows IoT Device Service 디바이스 할당,</span><span class="sxs-lookup"><span data-stu-id="37dbc-139">Windows IoT Device Service device allocation,</span></span>

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

### <span data-ttu-id="37dbc-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="37dbc-140">-ResourceGroupName</span></span>
<span data-ttu-id="37dbc-141">Windows IoT Device Service를 포함하는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="37dbc-141">The name of the resource group that contains the Windows IoT Device Service.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37dbc-142">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="37dbc-142">-SubscriptionId</span></span>
<span data-ttu-id="37dbc-143">구독 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="37dbc-143">The subscription identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37dbc-144">-Tag</span><span class="sxs-lookup"><span data-stu-id="37dbc-144">-Tag</span></span>
<span data-ttu-id="37dbc-145">리소스 태그.</span><span class="sxs-lookup"><span data-stu-id="37dbc-145">Resource tags.</span></span>

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

### <span data-ttu-id="37dbc-146">-Confirm</span><span class="sxs-lookup"><span data-stu-id="37dbc-146">-Confirm</span></span>
<span data-ttu-id="37dbc-147">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="37dbc-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="37dbc-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="37dbc-148">-WhatIf</span></span>
<span data-ttu-id="37dbc-149">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="37dbc-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="37dbc-150">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="37dbc-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="37dbc-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37dbc-151">CommonParameters</span></span>
<span data-ttu-id="37dbc-152">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="37dbc-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37dbc-153">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="37dbc-153">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37dbc-154">입력</span><span class="sxs-lookup"><span data-stu-id="37dbc-154">INPUTS</span></span>

### <span data-ttu-id="37dbc-155">Microsoft.Azure.PowerShell.Cmdlets.WindowsIotServices.Models.IWindowsIotServicesIdentity</span><span class="sxs-lookup"><span data-stu-id="37dbc-155">Microsoft.Azure.PowerShell.Cmdlets.WindowsIotServices.Models.IWindowsIotServicesIdentity</span></span>

## <span data-ttu-id="37dbc-156">출력</span><span class="sxs-lookup"><span data-stu-id="37dbc-156">OUTPUTS</span></span>

### <span data-ttu-id="37dbc-157">Microsoft.Azure.PowerShell.Cmdlets.WindowsIotServices.Models.Api20190601.IDeviceService</span><span class="sxs-lookup"><span data-stu-id="37dbc-157">Microsoft.Azure.PowerShell.Cmdlets.WindowsIotServices.Models.Api20190601.IDeviceService</span></span>

## <span data-ttu-id="37dbc-158">참고 사항</span><span class="sxs-lookup"><span data-stu-id="37dbc-158">NOTES</span></span>

<span data-ttu-id="37dbc-159">별칭</span><span class="sxs-lookup"><span data-stu-id="37dbc-159">ALIASES</span></span>

<span data-ttu-id="37dbc-160">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="37dbc-160">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="37dbc-161">아래에 설명된 매개 변수를 만들 수 있도록 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="37dbc-161">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="37dbc-162">해시 테이블에 대한 자세한 내용은 다음 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="37dbc-162">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="37dbc-163">INPUTOBJECT: <IWindowsIotServicesIdentity> ID 매개 변수</span><span class="sxs-lookup"><span data-stu-id="37dbc-163">INPUTOBJECT <IWindowsIotServicesIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="37dbc-164">`[DeviceName <String>]`: Windows IoT 디바이스 서비스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="37dbc-164">`[DeviceName <String>]`: The name of the Windows IoT Device Service.</span></span>
  - <span data-ttu-id="37dbc-165">`[Id <String>]`: 리소스 ID 경로</span><span class="sxs-lookup"><span data-stu-id="37dbc-165">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="37dbc-166">`[ResourceGroupName <String>]`: Windows IoT 디바이스 서비스를 포함하는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="37dbc-166">`[ResourceGroupName <String>]`: The name of the resource group that contains the Windows IoT Device Service.</span></span>
  - <span data-ttu-id="37dbc-167">`[SubscriptionId <String>]`: 구독 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="37dbc-167">`[SubscriptionId <String>]`: The subscription identifier.</span></span>

## <span data-ttu-id="37dbc-168">관련 링크</span><span class="sxs-lookup"><span data-stu-id="37dbc-168">RELATED LINKS</span></span>

