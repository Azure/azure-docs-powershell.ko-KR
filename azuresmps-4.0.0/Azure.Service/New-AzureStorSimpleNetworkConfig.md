---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 99D9EFA6-3506-4B0E-ACB5-C6EDBCB5A130
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9d73ede26d4bd85a39f4baf2090e581300eafb1b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045515"
---
# <span data-ttu-id="32b7c-101">New-AzureStorSimpleNetworkConfig</span><span class="sxs-lookup"><span data-stu-id="32b7c-101">New-AzureStorSimpleNetworkConfig</span></span>

## <span data-ttu-id="32b7c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="32b7c-102">SYNOPSIS</span></span>
<span data-ttu-id="32b7c-103">네트워크 구성 개체를 준비 합니다.</span><span class="sxs-lookup"><span data-stu-id="32b7c-103">Prepares a network configuration object.</span></span>

## <span data-ttu-id="32b7c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="32b7c-104">SYNTAX</span></span>

```
New-AzureStorSimpleNetworkConfig -InterfaceAlias <String> [-EnableIscsi <Boolean>] [-EnableCloud <Boolean>]
 [-Controller0IPv4Address <String>] [-Controller1IPv4Address <String>] [-IPv6Gateway <String>]
 [-IPv4Gateway <String>] [-IPv4Address <String>] [-IPv6Prefix <String>] [-IPv4Netmask <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="32b7c-105">설명은</span><span class="sxs-lookup"><span data-stu-id="32b7c-105">DESCRIPTION</span></span>
<span data-ttu-id="32b7c-106">**AzureStorSimpleNetworkConfig** Cmdlet은 **AzureStorSimpleDevice** cmdlet에 전달할 네트워크 구성 개체를 준비 합니다.</span><span class="sxs-lookup"><span data-stu-id="32b7c-106">The **New-AzureStorSimpleNetworkConfig** cmdlet prepares a network configuration object to pass to the **Set-AzureStorSimpleDevice** cmdlet.</span></span>
<span data-ttu-id="32b7c-107">Data0 인터페이스 에서만 *Controller0IPAddress* 매개 변수와 *Controller1IPAddress* 매개 변수를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="32b7c-107">Set the *Controller0IPAddress* parameter and *Controller1IPAddress* parameter only on the Data0 interface.</span></span>
<span data-ttu-id="32b7c-108">Data0는 *Controller0IPAddress* , *Controller1IPAdress* , *enableiscsi* 의 세 가지 설정만 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="32b7c-108">Data0 supports only three settings: *Controller0IPAddress* , *Controller1IPAdress* , and *EnableIscsi*.</span></span>

## <span data-ttu-id="32b7c-109">예제의</span><span class="sxs-lookup"><span data-stu-id="32b7c-109">EXAMPLES</span></span>

### <span data-ttu-id="32b7c-110">예제 1: Data0 인터페이스 구성</span><span class="sxs-lookup"><span data-stu-id="32b7c-110">Example 1: Configure a Data0 interface</span></span>
```
PS C:\>New-AzureStorSimpleNetworkConfig -InterfaceAlias Data0 -EnableIscsi $True -Controller0IPv4Address "10.67.64.48" -Controller1IPv4Address "10.67.64.49"
VERBOSE: ClientRequestId: 0621d220-a460-48ec-84ec-02a3a82f88b2_PS


IsIscsiEnabled         : True
IsCloudEnabled         : 
Controller0IPv4Address : 10.67.64.48
Controller1IPv4Address : 10.67.64.49
IPv6Gateway            : 
IPv4Gateway            : 
IPv4Address            : 
IPv6Prefix             : 
IPv4Netmask            : 
InterfaceAlias         : Data0

VERBOSE: Successfully created a StorSimple Network Configuration for interface Data0
```

<span data-ttu-id="32b7c-111">이 명령은 Data0 인터페이스에 대 한 네트워크 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="32b7c-111">This command creates network configuration for the Data0 interface.</span></span>
<span data-ttu-id="32b7c-112">이 명령은 *Controller0IPv4Address* , *Controller1IPv4Address* 및 *enableiscsi* 매개 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="32b7c-112">This command specifies the *Controller0IPv4Address* , *Controller1IPv4Address* , and *EnableIscsi* parameters.</span></span>
<span data-ttu-id="32b7c-113">이 cmdlet은 이러한 세 가지 매개 변수에 대해서만 Data0를 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="32b7c-113">This cmdlet can configure Data0 for only these three parameters.</span></span>

### <span data-ttu-id="32b7c-114">예제 2: Data0 이외의 인터페이스를</span><span class="sxs-lookup"><span data-stu-id="32b7c-114">Example 2: Configuren an interface other than Data0 an</span></span>
```
PS C:\>New-AzureStorSimpleNetworkConfig -InterfaceAlias Data1 -EnableIscsi $True -EnableCloud $True -IPv6Gateway "db8:421e:9a8::a4:1c50" -IPv4Gateway "10.67.64.1" -IPv4Address "10.67.64.48" -IPv6Prefix "2001:db8:a::123/64" -IPv4Netmask "255.255.0.0"
VERBOSE: ClientRequestId: 3a15ff0e-b769-4329-9147-676b1e0acd7d_PS


IsIscsiEnabled         : True
IsCloudEnabled         : True
Controller0IPv4Address : 
Controller1IPv4Address : 
IPv6Gateway            : db8:421e:9a8::a4:1c50
IPv4Gateway            : 10.67.64.1
IPv4Address            : 10.67.64.48
IPv6Prefix             : 2001:db8:a::123/64
IPv4Netmask            : 255.255.0.0
InterfaceAlias         : Data1
VERBOSE: Successfully created a StorSimple Network Configuration for interface Data1
```

<span data-ttu-id="32b7c-115">이 명령은 Data1 인터페이스를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="32b7c-115">This command configures the Data1 interface.</span></span>

### <span data-ttu-id="32b7c-116">예제 3: 장치에 대 한 구성 수정</span><span class="sxs-lookup"><span data-stu-id="32b7c-116">Example 3: Modify a configuration for a device</span></span>
```
PS C:\>$NetworkConfigData0 = New-AzureStorSimpleNetworkConfig -InterfaceAlias Data0 -EnableIscsi $True -Controller0IPv4Address "10.67.64.48" -Controller1IPv4Address "10.67.64.49"
$OnlineDevice = @(Get-AzureStorSimpleDevice | Where { $_.Status -eq "Online"})[0]
$UpdatedDetails = Set-AzureStorSimpleDevice -DeviceId $OnlineDevice.DeviceId -StorSimpleNetworkConfig $NetworkConfigData0
VERBOSE: ClientRequestId: 0f163163-5ad0-4635-a7b5-870d47297f66_PS
VERBOSE: Successfully created a StorSimple Network Configuration for interface Data0
VERBOSE: ClientRequestId: 552e4a6c-7006-4015-a20b-9def6428a85e_PS
VERBOSE: ClientRequestId: f31cc84c-bc8a-404a-9da6-4670a7999e75_PS
VERBOSE: 1 StorSimple device found! 
VERBOSE: ClientRequestId: 545bc1a9-3c1b-4e50-89a6-9678aefe79e5_PS
VERBOSE: ClientRequestId: f114ad08-47f5-4fb8-8a01-1ea7f1ed1b98_PS
VERBOSE: About to configure the device : newDeviceName ! 
VERBOSE: ClientRequestId: 6afe7927-1c19-48d3-ac22-68148fd056b8_PS
VERBOSE: The task created for your Setup operation has completed successfully. 
VERBOSE: ClientRequestId: 467c142c-90da-4d75-82a4-c114afce953d_PS
VERBOSE: Successfully updated configuration for device newDeviceName with id 865e68f6-1e71-47b6-80d5-15d3a23bd2b0
```

<span data-ttu-id="32b7c-117">첫 번째 명령은 Data0 인터페이스에 대 한 네트워크 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="32b7c-117">The first command creates a network configuration for the Data0 interface.</span></span>
<span data-ttu-id="32b7c-118">이 명령은 *Controller0IPv4Address* , *Controller1IPv4Address* 및 *enableiscsi* 매개 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="32b7c-118">This command specifies the *Controller0IPv4Address* , *Controller1IPv4Address* , and *EnableIscsi* parameters.</span></span>
<span data-ttu-id="32b7c-119">이 명령은 $NetworkConfigData 0 변수에 결과를 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="32b7c-119">The command stores the result in the $NetworkConfigData0 variable.</span></span>

<span data-ttu-id="32b7c-120">두 번째 명령은 **AzureStorSimpleDevice** Cmdlet 및 **Where-Object** core cmdlet을 사용 하 여 온라인 StorSimple 장치를 가져오고 $OnlineDevice 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="32b7c-120">The second command uses the **Get-AzureStorSimpleDevice** cmdlet and the **Where-Object** core cmdlet to get an online StorSimple device, and then stores it in the $OnlineDevice variable.</span></span>

<span data-ttu-id="32b7c-121">마지막 명령은 **Set-AzureStorSimpleDevice** cmdlet을 사용 하 여 지정 된 디바이스 ID의 장치에 대 한 구성을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="32b7c-121">The final command modifies the configuration for the device that has the specified device ID by using the **Set-AzureStorSimpleDevice** cmdlet.</span></span>
<span data-ttu-id="32b7c-122">명령에서 첫 번째 명령에 현재 cmdlet이 생성 하는 구성 개체를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="32b7c-122">The command uses the configuration object that the current cmdlet created in the first command.</span></span>

## <span data-ttu-id="32b7c-123">변수</span><span class="sxs-lookup"><span data-stu-id="32b7c-123">PARAMETERS</span></span>

### <span data-ttu-id="32b7c-124">-Controller0IPv4Address</span><span class="sxs-lookup"><span data-stu-id="32b7c-124">-Controller0IPv4Address</span></span>
<span data-ttu-id="32b7c-125">컨트롤러 0에 대 한 IPv4 주소를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="32b7c-125">Specifies the IPv4 address for controller 0.</span></span>
<span data-ttu-id="32b7c-126">Data0 인터페이스에만이 매개 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="32b7c-126">Specify this parameter only for the Data0 interface.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32b7c-127">-Controller1IPv4Address</span><span class="sxs-lookup"><span data-stu-id="32b7c-127">-Controller1IPv4Address</span></span>
<span data-ttu-id="32b7c-128">컨트롤러 1에 대 한 IPv4 주소를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="32b7c-128">Specifies the IPv4 address for controller 1.</span></span>
<span data-ttu-id="32b7c-129">Data0 인터페이스에만이 매개 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="32b7c-129">Specify this parameter only for the Data0 interface.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32b7c-130">-EnableCloud</span><span class="sxs-lookup"><span data-stu-id="32b7c-130">-EnableCloud</span></span>
<span data-ttu-id="32b7c-131">인터페이스를 클라우드와 사용할 수 있는지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="32b7c-131">Indicates whether to cloud-enable the interface.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32b7c-132">-EnableIscsi</span><span class="sxs-lookup"><span data-stu-id="32b7c-132">-EnableIscsi</span></span>
<span data-ttu-id="32b7c-133">인터페이스에 대해 인터넷 SCSI (ISCSI)를 사용할지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="32b7c-133">Indicates whether to enable Internet SCSI (ISCSI) for the interface.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32b7c-134">-인터페이스 별칭</span><span class="sxs-lookup"><span data-stu-id="32b7c-134">-InterfaceAlias</span></span>
<span data-ttu-id="32b7c-135">이 cmdlet이 설정을 제공 하는 인터페이스의 인터페이스 별칭을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="32b7c-135">Specifies the interface alias of interface for which this cmdlet supplies settings.</span></span>
<span data-ttu-id="32b7c-136">유효한 값은 Data0부터 Data5입니다.</span><span class="sxs-lookup"><span data-stu-id="32b7c-136">Valid values are from Data0 to Data5.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32b7c-137">-IPv4Address</span><span class="sxs-lookup"><span data-stu-id="32b7c-137">-IPv4Address</span></span>
<span data-ttu-id="32b7c-138">인터페이스에 대 한 IPv4 주소를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="32b7c-138">Specifies the IPv4 address for the interface.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32b7c-139">-IPv4Gateway</span><span class="sxs-lookup"><span data-stu-id="32b7c-139">-IPv4Gateway</span></span>
<span data-ttu-id="32b7c-140">게이트웨이의 IPv4 주소를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="32b7c-140">Specifies the IPv4 address of a gateway.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32b7c-141">-IPv4Netmask</span><span class="sxs-lookup"><span data-stu-id="32b7c-141">-IPv4Netmask</span></span>
<span data-ttu-id="32b7c-142">인터페이스에 대 한 IPv4 넷마스크를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="32b7c-142">Specifies the IPv4 netmask for the interface.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32b7c-143">-IPv6Gateway</span><span class="sxs-lookup"><span data-stu-id="32b7c-143">-IPv6Gateway</span></span>
<span data-ttu-id="32b7c-144">인터페이스에 대 한 IPv6 게이트웨이를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="32b7c-144">Specifies the IPv6 gateway for the interface.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32b7c-145">-IPv6Prefix</span><span class="sxs-lookup"><span data-stu-id="32b7c-145">-IPv6Prefix</span></span>
<span data-ttu-id="32b7c-146">인터페이스의 IPv6 접두사를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="32b7c-146">Specifies the IPv6 prefix for the interface.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32b7c-147">-프로필</span><span class="sxs-lookup"><span data-stu-id="32b7c-147">-Profile</span></span>
<span data-ttu-id="32b7c-148">Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="32b7c-148">Specifies an Azure profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32b7c-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="32b7c-149">CommonParameters</span></span>
<span data-ttu-id="32b7c-150">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="32b7c-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="32b7c-151">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="32b7c-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="32b7c-152">입력</span><span class="sxs-lookup"><span data-stu-id="32b7c-152">INPUTS</span></span>

### <span data-ttu-id="32b7c-153">않아야</span><span class="sxs-lookup"><span data-stu-id="32b7c-153">None</span></span>

## <span data-ttu-id="32b7c-154">출력</span><span class="sxs-lookup"><span data-stu-id="32b7c-154">OUTPUTS</span></span>

### <span data-ttu-id="32b7c-155">NetworkConfig</span><span class="sxs-lookup"><span data-stu-id="32b7c-155">NetworkConfig</span></span>
<span data-ttu-id="32b7c-156">이 cmdlet은 다음 속성을 포함 하는 NetworkConfig 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="32b7c-156">This cmdlet returns a NetworkConfig object that contains the following properties:</span></span> 

- <span data-ttu-id="32b7c-157">**IsIscsiEnabled** ( **부울** )</span><span class="sxs-lookup"><span data-stu-id="32b7c-157">**IsIscsiEnabled** ( **Boolean** )</span></span> 
- <span data-ttu-id="32b7c-158">**Iscloudenabled** ( **Boolean** )</span><span class="sxs-lookup"><span data-stu-id="32b7c-158">**IsCloudEnabled** ( **Boolean** )</span></span>
- <span data-ttu-id="32b7c-159">**Controller0IPv4Address** ( **IPAddress** )</span><span class="sxs-lookup"><span data-stu-id="32b7c-159">**Controller0IPv4Address** ( **IPAddress** )</span></span> 
- <span data-ttu-id="32b7c-160">**Controller1IPv4Address** ( **IPAddress** )</span><span class="sxs-lookup"><span data-stu-id="32b7c-160">**Controller1IPv4Address** ( **IPAddress** )</span></span> 
- <span data-ttu-id="32b7c-161">**IPv6Gateway** ( **IPAddress** )</span><span class="sxs-lookup"><span data-stu-id="32b7c-161">**IPv6Gateway** ( **IPAddress** )</span></span> 
- <span data-ttu-id="32b7c-162">**IPv4Gateway** ( **IPAddress** )</span><span class="sxs-lookup"><span data-stu-id="32b7c-162">**IPv4Gateway** ( **IPAddress** )</span></span> 
- <span data-ttu-id="32b7c-163">**IPv4Address** ( **IPAddress** )</span><span class="sxs-lookup"><span data-stu-id="32b7c-163">**IPv4Address** ( **IPAddress** )</span></span> 
- <span data-ttu-id="32b7c-164">**IPv6Prefix** ( **String** )</span><span class="sxs-lookup"><span data-stu-id="32b7c-164">**IPv6Prefix** ( **String** )</span></span>
- <span data-ttu-id="32b7c-165">**IPv4Netmask** ( **IPAddress** )</span><span class="sxs-lookup"><span data-stu-id="32b7c-165">**IPv4Netmask** ( **IPAddress** )</span></span> 
- <span data-ttu-id="32b7c-166">**NetInterfaceId** ( **인터페이스 별칭** )</span><span class="sxs-lookup"><span data-stu-id="32b7c-166">**InterfaceAlias** ( **NetInterfaceId** )</span></span>

## <span data-ttu-id="32b7c-167">상속자</span><span class="sxs-lookup"><span data-stu-id="32b7c-167">NOTES</span></span>

## <span data-ttu-id="32b7c-168">관련 링크</span><span class="sxs-lookup"><span data-stu-id="32b7c-168">RELATED LINKS</span></span>

[<span data-ttu-id="32b7c-169">Set-AzureStorSimpleDevice</span><span class="sxs-lookup"><span data-stu-id="32b7c-169">Set-AzureStorSimpleDevice</span></span>](./Set-AzureStorSimpleDevice.md)

[<span data-ttu-id="32b7c-170">Get-AzureStorSimpleDevice</span><span class="sxs-lookup"><span data-stu-id="32b7c-170">Get-AzureStorSimpleDevice</span></span>](./Get-AzureStorSimpleDevice.md)


