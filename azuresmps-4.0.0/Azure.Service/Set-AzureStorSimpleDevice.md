---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: AE8E6778-1299-4EC7-BFE0-3FB464AA7BB4
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7bea5cbf2b5e10c85aaafa43203c207193040464
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045753"
---
# <span data-ttu-id="f5e3d-101">Set-AzureStorSimpleDevice</span><span class="sxs-lookup"><span data-stu-id="f5e3d-101">Set-AzureStorSimpleDevice</span></span>

## <span data-ttu-id="f5e3d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f5e3d-102">SYNOPSIS</span></span>
<span data-ttu-id="f5e3d-103">장치에 대 한 장치 구성을 변경 합니다.</span><span class="sxs-lookup"><span data-stu-id="f5e3d-103">Changes the device configuration for a device.</span></span>

## <span data-ttu-id="f5e3d-104">구문과</span><span class="sxs-lookup"><span data-stu-id="f5e3d-104">SYNTAX</span></span>

### <span data-ttu-id="f5e3d-105">IdentifyByName (기본값)</span><span class="sxs-lookup"><span data-stu-id="f5e3d-105">IdentifyByName (Default)</span></span>
```
Set-AzureStorSimpleDevice -DeviceName <String> [-NewName <String>] [-TimeZone <TimeZoneInfo>]
 [-SecondaryDnsServer <String>] [-StorSimpleNetworkConfig <NetworkConfig[]>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="f5e3d-106">IdentifyById</span><span class="sxs-lookup"><span data-stu-id="f5e3d-106">IdentifyById</span></span>
```
Set-AzureStorSimpleDevice -DeviceId <String> [-NewName <String>] [-TimeZone <TimeZoneInfo>]
 [-SecondaryDnsServer <String>] [-StorSimpleNetworkConfig <NetworkConfig[]>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="f5e3d-107">설명은</span><span class="sxs-lookup"><span data-stu-id="f5e3d-107">DESCRIPTION</span></span>
<span data-ttu-id="f5e3d-108">**AzureStorSimpleDevice** cmdlet이 장치에 대 한 디바이스 구성을 변경 합니다.</span><span class="sxs-lookup"><span data-stu-id="f5e3d-108">The **Set-AzureStorSimpleDevice** cmdlet changes the device configuration for a device.</span></span>
<span data-ttu-id="f5e3d-109">처음으로 장치를 설정 하는 경우 *TimeZone* , *SecondaryDnsServer* 및 *StorSimpleNetworkConfig* 매개 변수를 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="f5e3d-109">If you are setting up a device for the first time, you must specify the *TimeZone* , *SecondaryDnsServer* , and *StorSimpleNetworkConfig* parameters.</span></span>
<span data-ttu-id="f5e3d-110">Controller0 및 controller1 및 IP 주소를 사용 하 여 Data0에 대 한 네트워크 구성을 포함 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="f5e3d-110">You must include network configuration for Data0 with controller0 and controller1 and IP addresses.</span></span>
<span data-ttu-id="f5e3d-111">장치를 처음 구성 하려면 하나 이상의 인터넷 SCSI (ISCSI) 사용 네트워크 인터페이스가 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="f5e3d-111">There must be at least one Internet SCSI (ISCSI)-enabled network interface to configure the device for the first time.</span></span>

## <span data-ttu-id="f5e3d-112">예제의</span><span class="sxs-lookup"><span data-stu-id="f5e3d-112">EXAMPLES</span></span>

### <span data-ttu-id="f5e3d-113">예제 1: 장치에 대 한 구성 수정</span><span class="sxs-lookup"><span data-stu-id="f5e3d-113">Example 1: Modify the configuration for a device</span></span>
```
PS C:\>$NetworkConfigData0 = New-AzureStorSimpleNetworkConfig -InterfaceAlias Data0 -EnableIscsi $True -Controller0IPv4Address "10.67.64.48" -Controller1IPv4Address "10.67.64.49" 
PS C:\> $TimeZoneInfo = [System.TimeZoneInfo]::GetSystemTimeZones() | where { $_.Id -eq "Pacific Standard Time" }
PS C:\> $OnlineDevice = @(Get-AzureStorSimpleDevice | Where { $_.Status -eq "Online"})[0]
PS C:\> $UpdatedDetails = Set-AzureStorSimpleDevice -DeviceId $OnlineDevice.DeviceId -NewName "Device22" -TimeZone $TimeZoneInfo -SecondaryDnsServer 10.8.8.8 -StorSimpleNetworkConfig $NetworkConfigData0
VERBOSE: ClientRequestId: 0f163163-5ad0-4635-a7b5-870d47297f66_PS
VERBOSE: Successfully created a StorSimple Network Configuration for interface Data0
VERBOSE: ClientRequestId: 552e4a6c-7006-4015-a20b-9def6428a85e_PS
VERBOSE: ClientRequestId: f31cc84c-bc8a-404a-9da6-4670a7999e75_PS
VERBOSE: 1 StorSimple device found! 
VERBOSE: ClientRequestId: 545bc1a9-3c1b-4e50-89a6-9678aefe79e5_PS
VERBOSE: ClientRequestId: f114ad08-47f5-4fb8-8a01-1ea7f1ed1b98_PS
VERBOSE: About to configure the device : Device22 ! 
VERBOSE: ClientRequestId: 6afe7927-1c19-48d3-ac22-68148fd056b8_PS
VERBOSE: The task created for your Setup operation has completed successfully. 
VERBOSE: ClientRequestId: 467c142c-90da-4d75-82a4-c114afce953d_PS
VERBOSE: Successfully updated configuration for device Device22 with id 865e68f6-1e71-47b6-80d5-15d3a23bd2b0
```

<span data-ttu-id="f5e3d-114">첫 번째 명령은 Data0 인터페이스에 대 한 네트워크 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="f5e3d-114">The first command creates a network configuration for the Data0 interface.</span></span>
<span data-ttu-id="f5e3d-115">이 명령은 *Controller0IPv4Address* , *Controller1IPv4Address* 및 *enableiscsi* 매개 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f5e3d-115">This command specifies the *Controller0IPv4Address* , *Controller1IPv4Address* , and *EnableIscsi* parameters.</span></span>
<span data-ttu-id="f5e3d-116">이 명령은 $NetworkConfigData 0 변수에 결과를 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="f5e3d-116">The command stores the result in the $NetworkConfigData0 variable.</span></span>

<span data-ttu-id="f5e3d-117">두 번째 명령은 **TimeZoneInfo** .net 클래스와 표준 구문을 사용 하 여 태평양 표준 시간대를 가져오고 해당 개체를 $TimeZoneInfo 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="f5e3d-117">The second command uses the **System.TimeZoneInfo** .NET class and standard syntax to get Pacific Standard Time zone, and stores that object in the $TimeZoneInfo variable.</span></span>

<span data-ttu-id="f5e3d-118">세 번째 명령은 **AzureStorSimpleDevice** Cmdlet 및 **Where-Object** core cmdlet을 사용 하 여 온라인 StorSimple 장치를 가져오고 $OnlineDevice 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="f5e3d-118">The third command uses the **Get-AzureStorSimpleDevice** cmdlet and the **Where-Object** core cmdlet to get an online StorSimple device, and then stores it in the $OnlineDevice variable.</span></span>

<span data-ttu-id="f5e3d-119">마지막 명령은 지정 된 디바이스 ID의 장치에 대 한 구성을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f5e3d-119">The final command modifies the configuration for the device that has the specified device ID.</span></span>
<span data-ttu-id="f5e3d-120">명령에서 첫 번째 명령에 현재 cmdlet이 생성 하는 구성 개체를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="f5e3d-120">The command uses the configuration object that the current cmdlet created in the first command.</span></span>
<span data-ttu-id="f5e3d-121">이 명령은 $TimeZoneInfo에 저장 된 표준 시간대를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="f5e3d-121">The command uses the time zone stored in $TimeZoneInfo.</span></span>

### <span data-ttu-id="f5e3d-122">예제 2: 장치를 수정 하는 구성 개체 파이프</span><span class="sxs-lookup"><span data-stu-id="f5e3d-122">Example 2: Pipe the configuration object to modify a device</span></span>
```
PS C:\>$TimeZoneInfo = [System.TimeZoneInfo]::GetSystemTimeZones() | where { $_.Id -eq "Pacific Standard Time" }
PS C:\> $OnlineDevice = @(Get-AzureStorSimpleDevice | Where { $_.Status -eq "Online"})[0]
PS C:\> $UpdatedDetails = New-AzureStorSimpleNetworkConfig -InterfaceAlias Data0 -EnableIscsi $True -Controller0IPv4Address "10.67.64.48" -Controller1IPv4Address "10.67.64.49" | Set-AzureStorSimpleDevice -DeviceId $OnlineDevice.DeviceId -NewName "Device22" -TimeZone $TimeZoneInfo -SecondaryDnsServer 10.8.8.8 
VERBOSE: ClientRequestId: fa2f5000-169c-4feb-abbf-23f4b5c837fa_PS
VERBOSE: Successfully created a StorSimple Network Configuration for interface Data0
VERBOSE: ClientRequestId: fae6a491-919c-44b2-93e0-0c51f202c24b_PS
VERBOSE: ClientRequestId: e1803427-a097-4d58-ab7d-14a4c39fd768_PS
VERBOSE: 1 StorSimple device found! 
VERBOSE: ClientRequestId: 9e796c3d-3100-46ab-9a09-0e10c73a296f_PS
VERBOSE: ClientRequestId: 5b4cad96-31f4-4d07-a278-df5af3e06ad4_PS
VERBOSE: About to configure the device : Device22 ! 
VERBOSE: ClientRequestId: 9061f7df-144f-4f30-858c-045d882ca392_PS
VERBOSE: The task created for your Setup operation has completed successfully. 
VERBOSE: ClientRequestId: 2ed2fa9b-8459-4cd6-9a61-5fc25ced2815_PS
VERBOSE: Successfully updated configuration for device Device22 with id 865e68f6-1e71-47b6-80d5-15d3a23bd2b0
```

<span data-ttu-id="f5e3d-123">이 예제에서는 마지막 명령이 파이프라인 연산자를 사용 하 여 현재 cmdlet에 네트워크 구성 개체를 전달 한다는 점을 제외 하 고 첫 번째 예제와 동일한 구성 업데이트를 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="f5e3d-123">This example does the same configuration update as the first example, except that the final command passes the network configuration object to the current cmdlet by using the pipeline operator.</span></span>

### <span data-ttu-id="f5e3d-124">예제 3: 장치를 수정할 표준 시간대 개체 파이프</span><span class="sxs-lookup"><span data-stu-id="f5e3d-124">Example 3: Pipe the time zone object to modify a device</span></span>
```
PS C:\>$NetworkConfigData0 = New-AzureStorSimpleNetworkConfig -InterfaceAlias Data0 -EnableIscsi $True -Controller0IPv4Address "10.67.64.48" -Controller1IPv4Address "10.67.64.49" 
PS C:\> $OnlineDevice = @(Get-AzureStorSimpleDevice | Where { $_.Status -eq "Online"})[0]
PS C:\> $UpdatedDetails = [System.TimeZoneInfo]::GetSystemTimeZones() | where { $_.Id -eq "Pacific Standard Time" } | Set-AzureStorSimpleDevice -DeviceId $OnlineDevice.DeviceId -NewName "Device22" -SecondaryDnsServer 10.8.8.8 -StorSimpleNetworkConfig $NetworkConfigData0
VERBOSE: ClientRequestId: cfc3f3c7-a8b6-462b-96f4-124050b736fe_PS
VERBOSE: Successfully created a StorSimple Network Configuration for interface Data0
VERBOSE: ClientRequestId: 6017b76f-a771-4bf8-901e-14876e0f9962_PS
VERBOSE: ClientRequestId: 59a9275c-9005-4e8a-b68b-efa1e6c27d47_PS
VERBOSE: 1 StorSimple device found! 
VERBOSE: ClientRequestId: 08e5142a-b038-4607-8690-0c5a8b948352_PS
VERBOSE: ClientRequestId: 218af244-b8f4-4a4b-817e-8f67e1323f03_PS
VERBOSE: About to configure the device : Device22 ! 
VERBOSE: ClientRequestId: fbd1f32d-1d74-432e-9dc0-90b46674884a_PS
VERBOSE: The task created for your Setup operation has completed successfully. 
VERBOSE: ClientRequestId: 981cb941-252c-4898-ba9f-f19e5b8bcaa4_PS
VERBOSE: Successfully updated configuration for device Device22 with id 865e68f6-1e71-47b6-80d5-15d3a23bd2b0
```

<span data-ttu-id="f5e3d-125">이 예제에서는 마지막 명령이 파이프라인 연산자를 사용 하 여 현재 cmdlet에 표준 시간대 개체를 전달 한다는 점을 제외 하 고 첫 번째 예제와 동일한 구성 업데이트를 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="f5e3d-125">This example does the same configuration update as the first example, except that the final command passes the time zone object to the current cmdlet by using the pipeline operator.</span></span>

## <span data-ttu-id="f5e3d-126">변수</span><span class="sxs-lookup"><span data-stu-id="f5e3d-126">PARAMETERS</span></span>

### <span data-ttu-id="f5e3d-127">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="f5e3d-127">-DeviceId</span></span>
<span data-ttu-id="f5e3d-128">구성할 StorSimple 장치의 인스턴스 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f5e3d-128">Specifies the instance ID of the StorSimple device to configure.</span></span>

```yaml
Type: String
Parameter Sets: IdentifyById
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5e3d-129">-장치 이름</span><span class="sxs-lookup"><span data-stu-id="f5e3d-129">-DeviceName</span></span>
<span data-ttu-id="f5e3d-130">구성할 StorSimple 장치의 친숙 한 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f5e3d-130">Specifies the friendly name of the StorSimple device to configure.</span></span>

```yaml
Type: String
Parameter Sets: IdentifyByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5e3d-131">-NewName</span><span class="sxs-lookup"><span data-stu-id="f5e3d-131">-NewName</span></span>
<span data-ttu-id="f5e3d-132">StorSimple 장치의 새 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f5e3d-132">Specifies the new friendly name of the StorSimple device.</span></span>

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

### <span data-ttu-id="f5e3d-133">-프로필</span><span class="sxs-lookup"><span data-stu-id="f5e3d-133">-Profile</span></span>
<span data-ttu-id="f5e3d-134">Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f5e3d-134">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="f5e3d-135">-SecondaryDnsServer</span><span class="sxs-lookup"><span data-stu-id="f5e3d-135">-SecondaryDnsServer</span></span>
<span data-ttu-id="f5e3d-136">StorSimple 장치에 대 한 보조 DNS 서버를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f5e3d-136">Specifies a secondary DNS server for the StorSimple device.</span></span>

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

### <span data-ttu-id="f5e3d-137">-StorSimpleNetworkConfig</span><span class="sxs-lookup"><span data-stu-id="f5e3d-137">-StorSimpleNetworkConfig</span></span>
<span data-ttu-id="f5e3d-138">디바이스의 인터페이스에 대 한 네트워크 구성 objectss의 배열을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f5e3d-138">Specifies an array of network configuration objectss for interfaces on a device.</span></span>
<span data-ttu-id="f5e3d-139">**Networkconfig** 개체를 얻으려면 New-AzureStorSimpleNetworkConfig cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="f5e3d-139">To obtain a **NetworkConfig** object, use the New-AzureStorSimpleNetworkConfig cmdlet.</span></span>

```yaml
Type: NetworkConfig[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f5e3d-140">-표준 시간대</span><span class="sxs-lookup"><span data-stu-id="f5e3d-140">-TimeZone</span></span>
<span data-ttu-id="f5e3d-141">장치에 대 한 표준 시간대를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f5e3d-141">Specifies a time zone for the device.</span></span>
<span data-ttu-id="f5e3d-142">**Getsystemtimezone ()** 메서드를 사용 하 여 **TimeZoneInfo** 개체를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f5e3d-142">You can create a **TimeZoneInfo** object by using the **GetSystemTimeZone()** method.</span></span>
<span data-ttu-id="f5e3d-143">예를 들어이 명령은 태평양 표준시에 대 한 표준 시간대 정보 개체를 만듭니다. `\[System.TimeZoneInfo\]::GetSystemTimeZones() | where { $_.Id -eq "Pacific Standard Time" }`</span><span class="sxs-lookup"><span data-stu-id="f5e3d-143">For example, this command creates a time zone information object for Pacific Standard Time: `\[System.TimeZoneInfo\]::GetSystemTimeZones() | where { $_.Id -eq "Pacific Standard Time" }`</span></span>

```yaml
Type: TimeZoneInfo
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f5e3d-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5e3d-144">CommonParameters</span></span>
<span data-ttu-id="f5e3d-145">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f5e3d-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5e3d-146">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f5e3d-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5e3d-147">입력</span><span class="sxs-lookup"><span data-stu-id="f5e3d-147">INPUTS</span></span>

### <span data-ttu-id="f5e3d-148">NetworkConfig, TimeZoneInfo</span><span class="sxs-lookup"><span data-stu-id="f5e3d-148">NetworkConfig, TimeZoneInfo</span></span>
<span data-ttu-id="f5e3d-149">이 cmdlet에 **Networkconfig** 개체 또는 **TimeZoneInfo** 를 파이프로 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f5e3d-149">You can pipe a **NetworkConfig** object or a **TimeZoneInfo** to this cmdlet.</span></span>

## <span data-ttu-id="f5e3d-150">출력</span><span class="sxs-lookup"><span data-stu-id="f5e3d-150">OUTPUTS</span></span>

### <span data-ttu-id="f5e3d-151">DeviceDetails</span><span class="sxs-lookup"><span data-stu-id="f5e3d-151">DeviceDetails</span></span>
<span data-ttu-id="f5e3d-152">이 cmdlet은 가상 장치에 대 한 업데이트 된 장치 세부 정보를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="f5e3d-152">This cmdlet returns updated device details for the virtual device.</span></span>

## <span data-ttu-id="f5e3d-153">상속자</span><span class="sxs-lookup"><span data-stu-id="f5e3d-153">NOTES</span></span>

## <span data-ttu-id="f5e3d-154">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f5e3d-154">RELATED LINKS</span></span>

[<span data-ttu-id="f5e3d-155">새로운 AzureStorSimpleNetworkConfig</span><span class="sxs-lookup"><span data-stu-id="f5e3d-155">New-AzureStorSimpleNetworkConfig</span></span>](./New-AzureStorSimpleNetworkConfig.md)

[<span data-ttu-id="f5e3d-156">Set-AzureStorSimpleVirtualDevice</span><span class="sxs-lookup"><span data-stu-id="f5e3d-156">Set-AzureStorSimpleVirtualDevice</span></span>](./Set-AzureStorSimpleVirtualDevice.md)


