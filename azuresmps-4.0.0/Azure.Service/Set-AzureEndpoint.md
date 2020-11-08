---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 1BA472FB-E684-486C-8066-42C9215DBDEF
online version: ''
schema: 2.0.0
ms.openlocfilehash: 83d1afcae66af7e4548b1dbd4031392969f4d267
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046057"
---
# <span data-ttu-id="a90d7-101">Set-AzureEndpoint</span><span class="sxs-lookup"><span data-stu-id="a90d7-101">Set-AzureEndpoint</span></span>

## <span data-ttu-id="a90d7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a90d7-102">SYNOPSIS</span></span>
<span data-ttu-id="a90d7-103">가상 컴퓨터에 할당 된 끝점을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a90d7-103">Modifies an endpoint assigned to a virtual machine.</span></span>

## <span data-ttu-id="a90d7-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a90d7-104">SYNTAX</span></span>

```
Set-AzureEndpoint [-Name] <String> [[-Protocol] <String>] [[-LocalPort] <Int32>] [-PublicPort <Int32>]
 [-DirectServerReturn <Boolean>] [-ACL <NetworkAclObject>] [-InternalLoadBalancerName <String>]
 [-IdleTimeoutInMinutes <Int32>] [-LoadBalancerDistribution <String>] [-VirtualIPName <String>]
 -VM <IPersistentVM> [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="a90d7-105">설명은</span><span class="sxs-lookup"><span data-stu-id="a90d7-105">DESCRIPTION</span></span>
<span data-ttu-id="a90d7-106">**Set azureendpoint** Cmdlet은 Azure 가상 컴퓨터에 할당 된 끝점을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a90d7-106">The **Set-AzureEndpoint** cmdlet modifies an endpoint assigned to an Azure virtual machine.</span></span>
<span data-ttu-id="a90d7-107">부하 분산 되지 않은 끝점에 대 한 변경 내용을 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a90d7-107">You can specify changes to an endpoint that is not load balanced.</span></span>

## <span data-ttu-id="a90d7-108">예제의</span><span class="sxs-lookup"><span data-stu-id="a90d7-108">EXAMPLES</span></span>

### <span data-ttu-id="a90d7-109">예제 1: 끝점을 수정 하 여 포트에서 수신</span><span class="sxs-lookup"><span data-stu-id="a90d7-109">Example 1: Modify an endpoint to listen on a port</span></span>
```
PS C:\> Get-AzureVM -ServiceName "ContosoService" -Name "VirutalMachine01" | Set-AzureEndpoint -Name "Web" -PublicPort 443 -LocalPort 443 -Protocol tcp | Update-AzureVM
```

<span data-ttu-id="a90d7-110">이 명령은 **get-help** cmdlet을 사용 하 여 VirtualMachine01 이라는 가상 컴퓨터의 구성을 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="a90d7-110">This command retrieves the configuration of a virtual machine named VirtualMachine01 by using the **Get-AzureVM** cmdlet.</span></span>
<span data-ttu-id="a90d7-111">이 명령은 파이프라인 연산자를 사용 하 여이를 현재 cmdlet에 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="a90d7-111">The command passes it to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="a90d7-112">이 cmdlet은 포트 443에서 수신 하도록 Web 이라는 끝점을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a90d7-112">This cmdlet modifies the endpoint named Web to listen on port 443.</span></span>
<span data-ttu-id="a90d7-113">이 명령은 가상 컴퓨터 개체를 **업데이트-add-azurevm** cmdlet에 전달 하 여 변경 내용을 구현 합니다.</span><span class="sxs-lookup"><span data-stu-id="a90d7-113">The command passes the virtual machine object to the **Update-AzureVM** cmdlet, which implements your changes.</span></span>

## <span data-ttu-id="a90d7-114">변수</span><span class="sxs-lookup"><span data-stu-id="a90d7-114">PARAMETERS</span></span>

### <span data-ttu-id="a90d7-115">-ACL</span><span class="sxs-lookup"><span data-stu-id="a90d7-115">-ACL</span></span>
<span data-ttu-id="a90d7-116">이 cmdlet이 끝점에 적용 하는 ACL (액세스 제어 목록) 구성 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a90d7-116">Specifies an access control list (ACL) configuration object that this cmdlet applies to the endpoint.</span></span>

```yaml
Type: NetworkAclObject
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a90d7-117">-DirectServerReturn</span><span class="sxs-lookup"><span data-stu-id="a90d7-117">-DirectServerReturn</span></span>
<span data-ttu-id="a90d7-118">이 cmdlet이 직접 서버 반환을 사용할 수 있는지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a90d7-118">Specifies whether this cmdlet enables direct server return.</span></span>
<span data-ttu-id="a90d7-119">사용할 $True를 지정 하거나 사용 하지 않을 $False.</span><span class="sxs-lookup"><span data-stu-id="a90d7-119">Specify $True to enable, or $False to disable.</span></span>

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

### <span data-ttu-id="a90d7-120">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="a90d7-120">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="a90d7-121">끝점에 대 한 TCP 유휴 시간 제한 기간 (분)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a90d7-121">Specifies the TCP idle time-out period, in minutes, for the endpoint.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a90d7-122">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="a90d7-122">-InformationAction</span></span>
<span data-ttu-id="a90d7-123">이 cmdlet이 정보 이벤트에 응답 하는 방법을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a90d7-123">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="a90d7-124">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="a90d7-124">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="a90d7-125">하기로</span><span class="sxs-lookup"><span data-stu-id="a90d7-125">Continue</span></span>
- <span data-ttu-id="a90d7-126">숨기기</span><span class="sxs-lookup"><span data-stu-id="a90d7-126">Ignore</span></span>
- <span data-ttu-id="a90d7-127">Inquire</span><span class="sxs-lookup"><span data-stu-id="a90d7-127">Inquire</span></span>
- <span data-ttu-id="a90d7-128">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="a90d7-128">SilentlyContinue</span></span>
- <span data-ttu-id="a90d7-129">중지가</span><span class="sxs-lookup"><span data-stu-id="a90d7-129">Stop</span></span>
- <span data-ttu-id="a90d7-130">대기</span><span class="sxs-lookup"><span data-stu-id="a90d7-130">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a90d7-131">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="a90d7-131">-InformationVariable</span></span>
<span data-ttu-id="a90d7-132">정보 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a90d7-132">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a90d7-133">-InternalLoadBalancerName</span><span class="sxs-lookup"><span data-stu-id="a90d7-133">-InternalLoadBalancerName</span></span>
<span data-ttu-id="a90d7-134">내부 부하 분산의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a90d7-134">Specifies the name of the internal load balancer.</span></span>

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

### <span data-ttu-id="a90d7-135">-LoadBalancerDistribution</span><span class="sxs-lookup"><span data-stu-id="a90d7-135">-LoadBalancerDistribution</span></span>
<span data-ttu-id="a90d7-136">부하 분산 장치 배포 알고리즘을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a90d7-136">Specifies the load balancer distribution algorithm.</span></span>
<span data-ttu-id="a90d7-137">유효한 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="a90d7-137">Valid values are:</span></span> 

- <span data-ttu-id="a90d7-138">sourceIP.</span><span class="sxs-lookup"><span data-stu-id="a90d7-138">sourceIP.</span></span>
<span data-ttu-id="a90d7-139">두 가지 튜플 선호도: 원본 IP, 대상 IP</span><span class="sxs-lookup"><span data-stu-id="a90d7-139">A two tuple affinity: Source IP, Destination IP</span></span> 
- <span data-ttu-id="a90d7-140">sourceIPProtocol.</span><span class="sxs-lookup"><span data-stu-id="a90d7-140">sourceIPProtocol.</span></span>
<span data-ttu-id="a90d7-141">세 가지 튜플 선호도: 원본 IP, 대상 IP, 프로토콜</span><span class="sxs-lookup"><span data-stu-id="a90d7-141">A three tuple affinity: Source IP, Destination IP, Protocol</span></span> 
- <span data-ttu-id="a90d7-142">않아야.</span><span class="sxs-lookup"><span data-stu-id="a90d7-142">none.</span></span>
<span data-ttu-id="a90d7-143">5 개의 튜플 선호도: 원본 IP, 원본 포트, 대상 IP, 대상 포트, 프로토콜</span><span class="sxs-lookup"><span data-stu-id="a90d7-143">A five tuple affinity: Source IP, Source Port, Destination IP, Destination Port, Protocol</span></span> 

<span data-ttu-id="a90d7-144">기본값은 없음입니다.</span><span class="sxs-lookup"><span data-stu-id="a90d7-144">The default value is none.</span></span>

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

### <span data-ttu-id="a90d7-145">-LocalPort</span><span class="sxs-lookup"><span data-stu-id="a90d7-145">-LocalPort</span></span>
<span data-ttu-id="a90d7-146">이 끝점에서 사용 하는 로컬, 개인 포트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a90d7-146">Specifies the local, private, port that this endpoint uses.</span></span>
<span data-ttu-id="a90d7-147">가상 컴퓨터 내의 응용 프로그램은이 끝점에 대 한 서비스 입력 요청에 대해이 포트에서 수신 대기 합니다.</span><span class="sxs-lookup"><span data-stu-id="a90d7-147">Applications within the virtual machine listen on this port for service input requests for this endpoint.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a90d7-148">-이름</span><span class="sxs-lookup"><span data-stu-id="a90d7-148">-Name</span></span>
<span data-ttu-id="a90d7-149">끝점의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a90d7-149">Specifies the name of the endpoint.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a90d7-150">-프로필</span><span class="sxs-lookup"><span data-stu-id="a90d7-150">-Profile</span></span>
<span data-ttu-id="a90d7-151">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a90d7-151">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="a90d7-152">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="a90d7-152">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="a90d7-153">-프로토콜</span><span class="sxs-lookup"><span data-stu-id="a90d7-153">-Protocol</span></span>
<span data-ttu-id="a90d7-154">끝점의 프로토콜을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a90d7-154">Specifies the protocol of the endpoint.</span></span>
<span data-ttu-id="a90d7-155">유효한 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="a90d7-155">Valid values are:</span></span> 

- <span data-ttu-id="a90d7-156">net.tcp</span><span class="sxs-lookup"><span data-stu-id="a90d7-156">tcp</span></span> 
- <span data-ttu-id="a90d7-157">udp</span><span class="sxs-lookup"><span data-stu-id="a90d7-157">udp</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a90d7-158">-PublicPort</span><span class="sxs-lookup"><span data-stu-id="a90d7-158">-PublicPort</span></span>
<span data-ttu-id="a90d7-159">끝점에서 사용 하는 공용 포트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a90d7-159">Specifies the public port that the endpoint uses.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a90d7-160">-VirtualIPName</span><span class="sxs-lookup"><span data-stu-id="a90d7-160">-VirtualIPName</span></span>
<span data-ttu-id="a90d7-161">Azure가 끝점에 연결 하는 가상 IP 주소의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a90d7-161">Specifies the name of a virtual IP address that Azure associates to the endpoint.</span></span>
<span data-ttu-id="a90d7-162">서비스에 여러 개의 가상 Ip가 있을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a90d7-162">Your service can have multiple virtual IPs.</span></span>
<span data-ttu-id="a90d7-163">가상 Ip를 만들려면 **Add-AzureVirtualIP** cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="a90d7-163">To create virtual IPs, use the **Add-AzureVirtualIP** cmdlet.</span></span>

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

### <span data-ttu-id="a90d7-164">-VM</span><span class="sxs-lookup"><span data-stu-id="a90d7-164">-VM</span></span>
<span data-ttu-id="a90d7-165">끝점이 속한 가상 컴퓨터를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a90d7-165">Specifies the virtual machine to which the endpoint belongs.</span></span>

```yaml
Type: IPersistentVM
Parameter Sets: (All)
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a90d7-166">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a90d7-166">CommonParameters</span></span>
<span data-ttu-id="a90d7-167">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a90d7-167">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a90d7-168">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a90d7-168">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a90d7-169">입력</span><span class="sxs-lookup"><span data-stu-id="a90d7-169">INPUTS</span></span>

## <span data-ttu-id="a90d7-170">출력</span><span class="sxs-lookup"><span data-stu-id="a90d7-170">OUTPUTS</span></span>

### <span data-ttu-id="a90d7-171">System. 개체</span><span class="sxs-lookup"><span data-stu-id="a90d7-171">System.Object</span></span>

## <span data-ttu-id="a90d7-172">상속자</span><span class="sxs-lookup"><span data-stu-id="a90d7-172">NOTES</span></span>

## <span data-ttu-id="a90d7-173">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a90d7-173">RELATED LINKS</span></span>

[<span data-ttu-id="a90d7-174">추가-AzureEndpoint</span><span class="sxs-lookup"><span data-stu-id="a90d7-174">Add-AzureEndpoint</span></span>](./Add-AzureEndpoint.md)

[<span data-ttu-id="a90d7-175">추가-AzureVirtualIP</span><span class="sxs-lookup"><span data-stu-id="a90d7-175">Add-AzureVirtualIP</span></span>](./Add-AzureVirtualIP.md)

[<span data-ttu-id="a90d7-176">Get-AzureEndpoint</span><span class="sxs-lookup"><span data-stu-id="a90d7-176">Get-AzureEndpoint</span></span>](./Get-AzureEndpoint.md)

[<span data-ttu-id="a90d7-177">다운로드-Add-azurevm</span><span class="sxs-lookup"><span data-stu-id="a90d7-177">Get-AzureVM</span></span>](./Get-AzureVM.md)

[<span data-ttu-id="a90d7-178">-AzureEndpoint 제거</span><span class="sxs-lookup"><span data-stu-id="a90d7-178">Remove-AzureEndpoint</span></span>](./Remove-AzureEndpoint.md)

[<span data-ttu-id="a90d7-179">업데이트-Add-azurevm</span><span class="sxs-lookup"><span data-stu-id="a90d7-179">Update-AzureVM</span></span>](./Update-AzureVM.md)


