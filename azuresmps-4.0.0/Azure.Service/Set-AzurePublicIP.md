---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: BFD4E4AD-8F1B-4E4E-BF52-435A6EEAA060
online version: ''
schema: 2.0.0
ms.openlocfilehash: 6beed021bfc12db3a3fdb1a66ee8ae6fe2e1e9b9
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045955"
---
# <span data-ttu-id="ea5c9-101">Set-AzurePublicIP</span><span class="sxs-lookup"><span data-stu-id="ea5c9-101">Set-AzurePublicIP</span></span>

## <span data-ttu-id="ea5c9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ea5c9-102">SYNOPSIS</span></span>
<span data-ttu-id="ea5c9-103">Azure 가상 컴퓨터에 공용 IP를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea5c9-103">Adds a Public IP to an Azure virtual machine.</span></span>

## <span data-ttu-id="ea5c9-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ea5c9-104">SYNTAX</span></span>

```
Set-AzurePublicIP [-PublicIPName] <String> [[-IdleTimeoutInMinutes] <Int32>] [[-DomainNameLabel] <String>]
 -VM <IPersistentVM> [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="ea5c9-105">설명은</span><span class="sxs-lookup"><span data-stu-id="ea5c9-105">DESCRIPTION</span></span>
<span data-ttu-id="ea5c9-106">**Set AzurePublicIP** Cmdlet은 Azure 가상 컴퓨터에 공용 IP를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea5c9-106">The **Set-AzurePublicIP** cmdlet adds a Public IP to an Azure virtual machine.</span></span>
<span data-ttu-id="ea5c9-107">기존 가상 컴퓨터에 대해이 cmdlet을 실행 하는 경우에는 가상 컴퓨터를 업데이트 하 여 변경 내용을 구현 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea5c9-107">If you run this cmdlet for an existing virtual machine, update the virtual machine to implement your changes.</span></span>
<span data-ttu-id="ea5c9-108">도메인 이름 레이블을 지정 하 여 공용 IP에 해당 하는 DNS 항목을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ea5c9-108">You can specify a domain name label to create a corresponding DNS entry for the public IP.</span></span>

## <span data-ttu-id="ea5c9-109">예제의</span><span class="sxs-lookup"><span data-stu-id="ea5c9-109">EXAMPLES</span></span>

### <span data-ttu-id="ea5c9-110">예제 1: 기존 가상 컴퓨터에 공용 IP 추가</span><span class="sxs-lookup"><span data-stu-id="ea5c9-110">Example 1: Add a Public IP to an existing virtual machine</span></span>
```
PS C:\> Get-AzureVM -ServiceName "FTPInAzure" -Name "FTPInstance" | Set-AzurePublicIP -PublicIPName "ftpip" | Update-AzureVM
```

<span data-ttu-id="ea5c9-111">이 명령은 ' Add-azurevm ' cmdlet을 사용 하 여 FTPInAzure 라는 서비스에서 가상 컴퓨터 (이름 **)** 인스턴스를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="ea5c9-111">This command gets the virtual machine named FTPInstance in the service named FTPInAzure by using the **Get-AzureVM** cmdlet.</span></span>
<span data-ttu-id="ea5c9-112">이 명령은 파이프라인 연산자를 사용 하 여 해당 가상 컴퓨터를 현재 cmdlet으로 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea5c9-112">The command passes that virtual machine to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="ea5c9-113">현재 cmdlet은 공용 IP 이름 (\ ip)을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea5c9-113">The current cmdlet adds the Public IP name ftpip.</span></span>
<span data-ttu-id="ea5c9-114">이 명령은 가상 컴퓨터를 **업데이트-add-azurevm** cmdlet에 전달 하 여 변경 내용을 구현 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea5c9-114">The command passes the virtual machine to the **Update-AzureVM** cmdlet, which implements your changes.</span></span>

### <span data-ttu-id="ea5c9-115">예제 2: 새 가상 컴퓨터에 공용 IP 추가</span><span class="sxs-lookup"><span data-stu-id="ea5c9-115">Example 2: Add a Public IP to a new virtual machine</span></span>
```
PS C:\> New-AzureVMConfig -Name "FTPInstance" -InstanceSize Small -ImageName "Image07" | Add-AzureProvisioningConfig -Windows -AdminUsername "AdminMain" -Password "password" | Set-AzurePublicIP -PublicIPName "ftpip" | New-AzureVM -ServiceName "FTPinAzure" -Location "North Central US"
```

<span data-ttu-id="ea5c9-116">이 명령은 **새 AzureVMConfig** cmdlet을 사용 하 여 가상 컴퓨터 구성 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ea5c9-116">This command creates a virtual machine configuration object by using the **New-AzureVMConfig** cmdlet.</span></span>
<span data-ttu-id="ea5c9-117">이 명령은 추가 구성을 제공 하는 **AzureProvisioningConfig** cmdlet에 해당 개체를 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea5c9-117">The command passes that object to the **Add-AzureProvisioningConfig** cmdlet, which provides additional configuration.</span></span>
<span data-ttu-id="ea5c9-118">현재 cmdlet은 공용 IP 이름 (\ ip)을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea5c9-118">The current cmdlet adds the Public IP name ftpip.</span></span>
<span data-ttu-id="ea5c9-119">이 명령은 가상 컴퓨터를 만드는 **새 add-azurevm** cmdlet에 구성을 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea5c9-119">The command passes the configuration to the **New-AzureVM** cmdlet, which creates the virtual machine.</span></span>

### <span data-ttu-id="ea5c9-120">예제 3: 공용 IP 및 레이블을 기존 가상 컴퓨터에 추가</span><span class="sxs-lookup"><span data-stu-id="ea5c9-120">Example 3: Add a Public IP and label to an existing virtual machine</span></span>
```
PS C:\> Get-AzureVM -ServiceName "FTPInAzure" -Name "FTPInstance" | Set-AzurePublicIP -PublicIPName "ftpip" -DomainNameLabel "ipname" | Update-AzureVM
```

<span data-ttu-id="ea5c9-121">이 명령은 ' Add-azurevm ' cmdlet을 사용 하 여 FTPInAzure 라는 서비스에서 가상 컴퓨터 (이름 **)** 인스턴스를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="ea5c9-121">This command gets the virtual machine named FTPInstance in the service named FTPInAzure by using the **Get-AzureVM** cmdlet.</span></span>
<span data-ttu-id="ea5c9-122">이 명령은 파이프라인 연산자를 사용 하 여 해당 가상 컴퓨터를 현재 cmdlet으로 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea5c9-122">The command passes that virtual machine to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="ea5c9-123">현재 cmdlet은 공용 IP 이름에는 ip 주소와 레이블 ipname을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea5c9-123">The current cmdlet adds the Public IP name ftpip and the label ipname.</span></span>
<span data-ttu-id="ea5c9-124">이 명령은 변경 내용을 구현 하는 가상 컴퓨터를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea5c9-124">The command updates the virtual machine, which implements your changes.</span></span>

### <span data-ttu-id="ea5c9-125">예제 4: 공용 IP 및 레이블을 새 가상 컴퓨터에 추가</span><span class="sxs-lookup"><span data-stu-id="ea5c9-125">Example 4: Add a Public IP and label to a new virtual machine</span></span>
```
PS C:\> New-AzureVMConfig -Name "FTPInstance" -InstanceSize Small -ImageName $images[50].ImageName | Add-AzureProvisioningConfig -Windows -AdminUsername "AdminMain" -Password "password" | Set-AzurePublicIP -PublicIPName "ftpip" -DomainNameLabel "ipname" | New-AzureVM -ServiceName "FTPinAzure" -Location "North Central US"
```

<span data-ttu-id="ea5c9-126">이 명령은 가상 컴퓨터 구성 개체를 만든 다음 추가 구성을 제공 하는 **AzureProvisioningConfig** 에 해당 개체를 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea5c9-126">This command creates a virtual machine configuration object, and then passes that object to **Add-AzureProvisioningConfig** , which provides additional configuration.</span></span>
<span data-ttu-id="ea5c9-127">현재 cmdlet은 공용 IP 이름에는 ip 주소와 레이블 ipname을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea5c9-127">The current cmdlet adds the Public IP name ftpip and the label ipname.</span></span>
<span data-ttu-id="ea5c9-128">명령이 가상 컴퓨터를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ea5c9-128">The command creates the virtual machine.</span></span>

## <span data-ttu-id="ea5c9-129">변수</span><span class="sxs-lookup"><span data-stu-id="ea5c9-129">PARAMETERS</span></span>

### <span data-ttu-id="ea5c9-130">-DomainNameLabel</span><span class="sxs-lookup"><span data-stu-id="ea5c9-130">-DomainNameLabel</span></span>
<span data-ttu-id="ea5c9-131">공용 IP 주소에 해당 하는 DNS 항목에 사용할 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea5c9-131">Specifies the name to use for a corresponding DNS entry for the public IP address.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea5c9-132">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="ea5c9-132">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="ea5c9-133">TCP 유휴 시간 제한 기간 (분)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea5c9-133">Specifies the TCP idle time-out period in minutes.</span></span>

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

### <span data-ttu-id="ea5c9-134">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="ea5c9-134">-InformationAction</span></span>
<span data-ttu-id="ea5c9-135">이 cmdlet이 정보 이벤트에 응답 하는 방법을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea5c9-135">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="ea5c9-136">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="ea5c9-136">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="ea5c9-137">하기로</span><span class="sxs-lookup"><span data-stu-id="ea5c9-137">Continue</span></span>
- <span data-ttu-id="ea5c9-138">숨기기</span><span class="sxs-lookup"><span data-stu-id="ea5c9-138">Ignore</span></span>
- <span data-ttu-id="ea5c9-139">Inquire</span><span class="sxs-lookup"><span data-stu-id="ea5c9-139">Inquire</span></span>
- <span data-ttu-id="ea5c9-140">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="ea5c9-140">SilentlyContinue</span></span>
- <span data-ttu-id="ea5c9-141">중지가</span><span class="sxs-lookup"><span data-stu-id="ea5c9-141">Stop</span></span>
- <span data-ttu-id="ea5c9-142">대기</span><span class="sxs-lookup"><span data-stu-id="ea5c9-142">Suspend</span></span>

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

### <span data-ttu-id="ea5c9-143">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="ea5c9-143">-InformationVariable</span></span>
<span data-ttu-id="ea5c9-144">정보 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea5c9-144">Specifies an information variable.</span></span>

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

### <span data-ttu-id="ea5c9-145">-프로필</span><span class="sxs-lookup"><span data-stu-id="ea5c9-145">-Profile</span></span>
<span data-ttu-id="ea5c9-146">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea5c9-146">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="ea5c9-147">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="ea5c9-147">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="ea5c9-148">-PublicIPName</span><span class="sxs-lookup"><span data-stu-id="ea5c9-148">-PublicIPName</span></span>
<span data-ttu-id="ea5c9-149">공용 IP 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea5c9-149">Specifies the Public IP name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea5c9-150">-VM</span><span class="sxs-lookup"><span data-stu-id="ea5c9-150">-VM</span></span>
<span data-ttu-id="ea5c9-151">이 cmdlet이 공용 IP를 추가 하는 가상 컴퓨터를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea5c9-151">Specifies the virtual machine to which this cmdlet adds Public IP.</span></span>

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

### <span data-ttu-id="ea5c9-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea5c9-152">CommonParameters</span></span>
<span data-ttu-id="ea5c9-153">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea5c9-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea5c9-154">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ea5c9-154">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea5c9-155">입력</span><span class="sxs-lookup"><span data-stu-id="ea5c9-155">INPUTS</span></span>

## <span data-ttu-id="ea5c9-156">출력</span><span class="sxs-lookup"><span data-stu-id="ea5c9-156">OUTPUTS</span></span>

### <span data-ttu-id="ea5c9-157">WindowsAzure. ServiceManagement. IPersistentVM</span><span class="sxs-lookup"><span data-stu-id="ea5c9-157">Microsoft.WindowsAzure.Commands.ServiceManagement.Model.IPersistentVM</span></span>

## <span data-ttu-id="ea5c9-158">상속자</span><span class="sxs-lookup"><span data-stu-id="ea5c9-158">NOTES</span></span>

## <span data-ttu-id="ea5c9-159">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ea5c9-159">RELATED LINKS</span></span>

[<span data-ttu-id="ea5c9-160">Get-AzurePublicIP</span><span class="sxs-lookup"><span data-stu-id="ea5c9-160">Get-AzurePublicIP</span></span>](./Get-AzurePublicIP.md)

[<span data-ttu-id="ea5c9-161">다운로드-Add-azurevm</span><span class="sxs-lookup"><span data-stu-id="ea5c9-161">Get-AzureVM</span></span>](./Get-AzureVM.md)

[<span data-ttu-id="ea5c9-162">뉴욕</span><span class="sxs-lookup"><span data-stu-id="ea5c9-162">New-AzureVM</span></span>](./New-AzureVM.md)

[<span data-ttu-id="ea5c9-163">새로운 AzureVMConfig</span><span class="sxs-lookup"><span data-stu-id="ea5c9-163">New-AzureVMConfig</span></span>](./New-AzureVMConfig.md)

[<span data-ttu-id="ea5c9-164">제거-AzurePublicIP</span><span class="sxs-lookup"><span data-stu-id="ea5c9-164">Remove-AzurePublicIP</span></span>](./Remove-AzurePublicIP.md)

[<span data-ttu-id="ea5c9-165">업데이트-Add-azurevm</span><span class="sxs-lookup"><span data-stu-id="ea5c9-165">Update-AzureVM</span></span>](./Update-AzureVM.md)


