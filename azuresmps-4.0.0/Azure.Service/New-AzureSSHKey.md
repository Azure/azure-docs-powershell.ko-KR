---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: AA58B897-EFA0-4321-9246-ED8E11AB3538
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7a0e0d5cac7ac27bf7eeefe8e3eb995a82a32ea4
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045982"
---
# <span data-ttu-id="ff542-101">New-AzureSSHKey</span><span class="sxs-lookup"><span data-stu-id="ff542-101">New-AzureSSHKey</span></span>

## <span data-ttu-id="ff542-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ff542-102">SYNOPSIS</span></span>
<span data-ttu-id="ff542-103">기존 인증서를 새 Linux 기반 Azure 가상 컴퓨터에 삽입 하는 SSH 키 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ff542-103">Creates a SSH Key object to insert an existing certificate into a new Linux-based Azure virtual machines.</span></span>

## <span data-ttu-id="ff542-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ff542-104">SYNTAX</span></span>

### <span data-ttu-id="ff542-105">쌍</span><span class="sxs-lookup"><span data-stu-id="ff542-105">keypair</span></span>
```
New-AzureSSHKey [-KeyPair] [-Fingerprint] <String> [-Path] <String> [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="ff542-106">publickey</span><span class="sxs-lookup"><span data-stu-id="ff542-106">publickey</span></span>
```
New-AzureSSHKey [-PublicKey] [-Fingerprint] <String> [-Path] <String> [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="ff542-107">설명은</span><span class="sxs-lookup"><span data-stu-id="ff542-107">DESCRIPTION</span></span>
<span data-ttu-id="ff542-108">**AzureSSHKey** cmdlet은 이미 Azure에 추가 된 인증서에 대 한 SSH 키 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ff542-108">The **New-AzureSSHKey** cmdlet creates an SSH Key object for a certificate that has already been added to Azure.</span></span>
<span data-ttu-id="ff542-109">이 SSH 키 개체 **는 뉴욕을 사용 하** 여 새 가상 컴퓨터에 대 한 구성 개체를 만들거나 **new-AzureQuickVM** 가 있는 새 가상 컴퓨터를 만들 때 **AzureProvisioningConfig** 에서 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ff542-109">This SSH Key object can then be used by **New-AzureProvisioningConfig** when creating the configuration object for a new virtual machine using **New-AzureVM** , or when creating a new virtual machine with **New-AzureQuickVM**.</span></span>
<span data-ttu-id="ff542-110">가상 컴퓨터 만들기 스크립트의 일부로 포함 되는 경우 지정 된 SSH 공개 키 또는 키 쌍이 새 가상 컴퓨터에 추가 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ff542-110">When included as part of a virtual machine creation script, this adds the specified SSH Public Key or Key Pair to the new virtual machine.</span></span>

## <span data-ttu-id="ff542-111">예제의</span><span class="sxs-lookup"><span data-stu-id="ff542-111">EXAMPLES</span></span>

### <span data-ttu-id="ff542-112">예제 1: 인증서 설정 개체 만들기</span><span class="sxs-lookup"><span data-stu-id="ff542-112">Example 1: Create a certificate setting object</span></span>
```
PS C:\> $myLxCert = New-AzureSSHKey -Fingerprint "D7BECD4D63EBAF86023BB4F1A5FBF5C2C924902A" -Path "/home/username/.ssh/authorized_keys"
```

<span data-ttu-id="ff542-113">이 명령은 기존 인증서에 대 한 인증서 설정 개체를 만든 다음 나중에 사용 하기 위해 변수에 개체를 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="ff542-113">This command creates a certificate setting object for an existing certificate and then stores the object in a variable for later use.</span></span>

### <span data-ttu-id="ff542-114">예제 2: 서비스에 인증서 추가</span><span class="sxs-lookup"><span data-stu-id="ff542-114">Example 2: Add a certificate to a service</span></span>
```
PS C:\> Add-AzureCertificate -ServiceName "MySvc" -CertToDeploy "C:\temp\MyLxCert.cer"
$myLxCert = New-AzureSSHKey ?Fingerprint "D7BECD4D63EBAF86023BB4F1A5FBF5C2C924902A" -Path "/home/username/.ssh/authorized_keys"
New-AzureVMConfig -Name "MyVM2" -InstanceSize Small -ImageName $LxImage `
          | Add-AzureProvisioningConfig -Linux -LinuxUser $lxUser -SSHPublicKeys $myLxCert -Password 'pass@word1' `
          | New-AzureVM -ServiceName "MySvc"
```

<span data-ttu-id="ff542-115">이 명령은 Azure 서비스에 인증서를 추가한 다음 인증서를 사용 하는 새 Linux 가상 컴퓨터를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ff542-115">This command adds a certificate to an Azure service, and then creates a new Linux virtual machine that uses the certificate.</span></span>

## <span data-ttu-id="ff542-116">변수</span><span class="sxs-lookup"><span data-stu-id="ff542-116">PARAMETERS</span></span>

### <span data-ttu-id="ff542-117">-지문</span><span class="sxs-lookup"><span data-stu-id="ff542-117">-Fingerprint</span></span>
<span data-ttu-id="ff542-118">인증서의 지문을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ff542-118">Specifies the fingerprint of the certificate.</span></span>

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

### <span data-ttu-id="ff542-119">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="ff542-119">-InformationAction</span></span>
<span data-ttu-id="ff542-120">이 cmdlet이 정보 이벤트에 응답 하는 방법을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ff542-120">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="ff542-121">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="ff542-121">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="ff542-122">하기로</span><span class="sxs-lookup"><span data-stu-id="ff542-122">Continue</span></span>
- <span data-ttu-id="ff542-123">숨기기</span><span class="sxs-lookup"><span data-stu-id="ff542-123">Ignore</span></span>
- <span data-ttu-id="ff542-124">Inquire</span><span class="sxs-lookup"><span data-stu-id="ff542-124">Inquire</span></span>
- <span data-ttu-id="ff542-125">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="ff542-125">SilentlyContinue</span></span>
- <span data-ttu-id="ff542-126">중지가</span><span class="sxs-lookup"><span data-stu-id="ff542-126">Stop</span></span>
- <span data-ttu-id="ff542-127">대기</span><span class="sxs-lookup"><span data-stu-id="ff542-127">Suspend</span></span>

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

### <span data-ttu-id="ff542-128">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="ff542-128">-InformationVariable</span></span>
<span data-ttu-id="ff542-129">정보 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ff542-129">Specifies an information variable.</span></span>

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

### <span data-ttu-id="ff542-130">-키 쌍</span><span class="sxs-lookup"><span data-stu-id="ff542-130">-KeyPair</span></span>
<span data-ttu-id="ff542-131">이 cmdlet이 새 가상 컴퓨터 구성에 SSH 키 쌍을 삽입 하기 위한 개체를 만들기 위해 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ff542-131">Specifies that this cmdlet creates an object for inserting an SSH Key Pair into the new virtual machine configuration.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: keypair
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff542-132">-Path</span><span class="sxs-lookup"><span data-stu-id="ff542-132">-Path</span></span>
<span data-ttu-id="ff542-133">SSH 공개 키 또는 키 쌍을 저장할 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ff542-133">Specifies the path to store the SSH Public Key or Key Pair.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff542-134">-PublicKey</span><span class="sxs-lookup"><span data-stu-id="ff542-134">-PublicKey</span></span>
<span data-ttu-id="ff542-135">이 cmdlet이 새 가상 컴퓨터 구성에 SSH 공개 키를 삽입 하기 위한 개체를 만들기 위해 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ff542-135">Specifies that this cmdlet creates an object for inserting an SSH Public Key into the new virtual machine configuration.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: publickey
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff542-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff542-136">CommonParameters</span></span>
<span data-ttu-id="ff542-137">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ff542-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff542-138">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ff542-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff542-139">입력</span><span class="sxs-lookup"><span data-stu-id="ff542-139">INPUTS</span></span>

## <span data-ttu-id="ff542-140">출력</span><span class="sxs-lookup"><span data-stu-id="ff542-140">OUTPUTS</span></span>

## <span data-ttu-id="ff542-141">상속자</span><span class="sxs-lookup"><span data-stu-id="ff542-141">NOTES</span></span>

## <span data-ttu-id="ff542-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ff542-142">RELATED LINKS</span></span>

[<span data-ttu-id="ff542-143">추가-AzureProvisioningConfig</span><span class="sxs-lookup"><span data-stu-id="ff542-143">Add-AzureProvisioningConfig</span></span>](./Add-AzureProvisioningConfig.md)

[<span data-ttu-id="ff542-144">새로운 AzureVMConfig</span><span class="sxs-lookup"><span data-stu-id="ff542-144">New-AzureVMConfig</span></span>](./New-AzureVMConfig.md)

[<span data-ttu-id="ff542-145">뉴욕</span><span class="sxs-lookup"><span data-stu-id="ff542-145">New-AzureVM</span></span>](./New-AzureVM.md)

[<span data-ttu-id="ff542-146">새로운 AzureQuickVM</span><span class="sxs-lookup"><span data-stu-id="ff542-146">New-AzureQuickVM</span></span>](./New-AzureQuickVM.md)


