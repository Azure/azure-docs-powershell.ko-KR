---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 11919623-9EDF-42A3-93FE-54E93D76D3D0
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7492dbdea0f924e364ac1acf5ce30476e34782d6
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045932"
---
# <span data-ttu-id="23a8b-101">New-AzureCertificateSetting</span><span class="sxs-lookup"><span data-stu-id="23a8b-101">New-AzureCertificateSetting</span></span>

## <span data-ttu-id="23a8b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="23a8b-102">SYNOPSIS</span></span>
<span data-ttu-id="23a8b-103">인증서에 대 한 인증서 설정 개체를 서비스에 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="23a8b-103">Creates a certificate setting object for a certificate is in a service.</span></span>

## <span data-ttu-id="23a8b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="23a8b-104">SYNTAX</span></span>

```
New-AzureCertificateSetting [[-StoreName] <String>] [-Thumbprint] <String>
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="23a8b-105">설명은</span><span class="sxs-lookup"><span data-stu-id="23a8b-105">DESCRIPTION</span></span>
<span data-ttu-id="23a8b-106">**AzureCertificateSetting** Cmdlet은 Azure 서비스에 있는 인증서에 대 한 인증서 설정 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="23a8b-106">The **New-AzureCertificateSetting** cmdlet creates a certificate setting object for a certificate that is in an Azure service.</span></span>

<span data-ttu-id="23a8b-107">인증서 설정 개체를 사용 하 여 **추가-AzureProvisioningConfig** cmdlet을 사용 하 여 구성 개체를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="23a8b-107">You can use a certificate setting object to create a configuration object by using the **Add-AzureProvisioningConfig** cmdlet.</span></span>
<span data-ttu-id="23a8b-108">구성 개체를 사용 하 여 **새 add-azurevm** cmdlet을 사용 하 여 가상 컴퓨터를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="23a8b-108">Use a configuration object to create virtual machine by using the **New-AzureVM** cmdlet.</span></span>
<span data-ttu-id="23a8b-109">인증서 설정 개체를 사용 하 여 **새 AzureQuickVM** cmdlet을 사용 하 여 가상 컴퓨터를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="23a8b-109">You can use a certificate setting object to create a virtual machine by using the **New-AzureQuickVM** cmdlet.</span></span>

## <span data-ttu-id="23a8b-110">예제의</span><span class="sxs-lookup"><span data-stu-id="23a8b-110">EXAMPLES</span></span>

### <span data-ttu-id="23a8b-111">예제 1: 인증서 설정 개체 만들기</span><span class="sxs-lookup"><span data-stu-id="23a8b-111">Example 1: Create a certificate setting object</span></span>
```
PS C:\> New-AzureCertificateSetting -Thumbprint "D7BECD4D63EBAF86023BB41FA5FBF5C2C924902A" -StoreName "My"
```

<span data-ttu-id="23a8b-112">이 명령은 기존 인증서에 대 한 인증서 설정 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="23a8b-112">This command creates a certificate setting object for an existing certificate.</span></span>

### <span data-ttu-id="23a8b-113">예제 2: 구성 설정 개체를 사용 하는 가상 컴퓨터 만들기</span><span class="sxs-lookup"><span data-stu-id="23a8b-113">Example 2: Create a virtual machine that uses a configuration setting object</span></span>
```
PS C:\> Add-AzureCertificate -ServiceName "ContosoService" -CertToDeploy "C:\temp\ContosoCert.cer"
PS C:\> $CertificateSetting = New-AzureCertificateSetting -Thumbprint "D7BECD4D63EBAF86023BB41FA5FBF5C2C924902A" -StoreName "My" 
PS C:\> $Image = Get-AzureVMImage -ImageName "ContosoStandard"
PS C:\> New-AzureVMConfig -Name "VirtualMachine17" -InstanceSize Small -ImageName $Image | Add-AzureProvisioningConfig -Windows -Certificates $CertificateSetting -Password "password" | New-AzureVM -ServiceName "ContosoService"
```

<span data-ttu-id="23a8b-114">첫 번째 명령은 **AzureCertificate** cmdlet을 사용 하 여 ContosoService 이라는 인증서 ContosoCert를 서비스에 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="23a8b-114">The first command adds the certificate ContosoCert.cer to the service named ContosoService by using the **Add-AzureCertificate** cmdlet.</span></span>

<span data-ttu-id="23a8b-115">두 번째 명령은 인증서 설정 개체를 만든 다음 $CertificateSetting 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="23a8b-115">The second command creates a certificate setting object, and then stores it in the $CertificateSetting variable.</span></span>

<span data-ttu-id="23a8b-116">세 번째 명령은 **AzureVMImage** cmdlet을 사용 하 여 이미지 리포지토리에서 이미지를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="23a8b-116">The third command gets an image from the image repository by using the **Get-AzureVMImage** cmdlet.</span></span>
<span data-ttu-id="23a8b-117">이 명령은 $Image 변수에 이미지를 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="23a8b-117">This command store the image in the $Image variable.</span></span>

<span data-ttu-id="23a8b-118">마지막 명령은 **AzureVMConfig** cmdlet을 사용 하 여 $Image의 이미지를 기반으로 가상 컴퓨터 구성 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="23a8b-118">The final command creates a virtual machine configuration object based on the image in $Image by using the **New-AzureVMConfig** cmdlet.</span></span>
<span data-ttu-id="23a8b-119">이 명령은 파이프라인 연산자를 사용 하 여 **AzureProvisioningConfig** cmdlet에 해당 개체를 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="23a8b-119">The command passes that object to the **Add-AzureProvisioningConfig** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="23a8b-120">해당 cmdlet은 구성에 프로 비전 정보를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="23a8b-120">That cmdlet add provisioning information to the configuration.</span></span>
<span data-ttu-id="23a8b-121">이 명령은 가상 컴퓨터를 만드는 **새 add-azurevm** cmdlet에 개체를 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="23a8b-121">The command passes the object to the **New-AzureVM** cmdlet, which creates the virtual machine.</span></span>

## <span data-ttu-id="23a8b-122">변수</span><span class="sxs-lookup"><span data-stu-id="23a8b-122">PARAMETERS</span></span>

### <span data-ttu-id="23a8b-123">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="23a8b-123">-InformationAction</span></span>
<span data-ttu-id="23a8b-124">이 cmdlet이 정보 이벤트에 응답 하는 방법을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="23a8b-124">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="23a8b-125">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="23a8b-125">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="23a8b-126">하기로</span><span class="sxs-lookup"><span data-stu-id="23a8b-126">Continue</span></span>
- <span data-ttu-id="23a8b-127">숨기기</span><span class="sxs-lookup"><span data-stu-id="23a8b-127">Ignore</span></span>
- <span data-ttu-id="23a8b-128">Inquire</span><span class="sxs-lookup"><span data-stu-id="23a8b-128">Inquire</span></span>
- <span data-ttu-id="23a8b-129">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="23a8b-129">SilentlyContinue</span></span>
- <span data-ttu-id="23a8b-130">중지가</span><span class="sxs-lookup"><span data-stu-id="23a8b-130">Stop</span></span>
- <span data-ttu-id="23a8b-131">대기</span><span class="sxs-lookup"><span data-stu-id="23a8b-131">Suspend</span></span>

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

### <span data-ttu-id="23a8b-132">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="23a8b-132">-InformationVariable</span></span>
<span data-ttu-id="23a8b-133">정보 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="23a8b-133">Specifies an information variable.</span></span>

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

### <span data-ttu-id="23a8b-134">-StoreName</span><span class="sxs-lookup"><span data-stu-id="23a8b-134">-StoreName</span></span>
<span data-ttu-id="23a8b-135">인증서를 저장할 인증서 저장소를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="23a8b-135">Specifies the certificate store in which to put the certificate.</span></span>
<span data-ttu-id="23a8b-136">유효한 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="23a8b-136">Valid values are:</span></span> 

- <span data-ttu-id="23a8b-137">주소록</span><span class="sxs-lookup"><span data-stu-id="23a8b-137">AddressBook</span></span>
- <span data-ttu-id="23a8b-138">AuthRoot</span><span class="sxs-lookup"><span data-stu-id="23a8b-138">AuthRoot</span></span>
- <span data-ttu-id="23a8b-139">CertificateAuthority</span><span class="sxs-lookup"><span data-stu-id="23a8b-139">CertificateAuthority</span></span>
- <span data-ttu-id="23a8b-140">허가</span><span class="sxs-lookup"><span data-stu-id="23a8b-140">Disallowed</span></span>
- <span data-ttu-id="23a8b-141">내</span><span class="sxs-lookup"><span data-stu-id="23a8b-141">My</span></span>
- <span data-ttu-id="23a8b-142">루트</span><span class="sxs-lookup"><span data-stu-id="23a8b-142">Root</span></span>
- <span data-ttu-id="23a8b-143">개인 사용자</span><span class="sxs-lookup"><span data-stu-id="23a8b-143">TrustedPeople</span></span>
- <span data-ttu-id="23a8b-144">용 게시자</span><span class="sxs-lookup"><span data-stu-id="23a8b-144">TrustedPublisher</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23a8b-145">-지문</span><span class="sxs-lookup"><span data-stu-id="23a8b-145">-Thumbprint</span></span>
<span data-ttu-id="23a8b-146">인증서의 지문을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="23a8b-146">Specifies the thumbprint of the certificate.</span></span>

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

### <span data-ttu-id="23a8b-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23a8b-147">CommonParameters</span></span>
<span data-ttu-id="23a8b-148">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="23a8b-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23a8b-149">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="23a8b-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23a8b-150">입력</span><span class="sxs-lookup"><span data-stu-id="23a8b-150">INPUTS</span></span>

## <span data-ttu-id="23a8b-151">출력</span><span class="sxs-lookup"><span data-stu-id="23a8b-151">OUTPUTS</span></span>

## <span data-ttu-id="23a8b-152">상속자</span><span class="sxs-lookup"><span data-stu-id="23a8b-152">NOTES</span></span>

## <span data-ttu-id="23a8b-153">관련 링크</span><span class="sxs-lookup"><span data-stu-id="23a8b-153">RELATED LINKS</span></span>

[<span data-ttu-id="23a8b-154">추가-AzureCertificate</span><span class="sxs-lookup"><span data-stu-id="23a8b-154">Add-AzureCertificate</span></span>](./Add-AzureCertificate.md)

[<span data-ttu-id="23a8b-155">추가-AzureProvisioningConfig</span><span class="sxs-lookup"><span data-stu-id="23a8b-155">Add-AzureProvisioningConfig</span></span>](./Add-AzureProvisioningConfig.md)

[<span data-ttu-id="23a8b-156">Get-AzureCertificate</span><span class="sxs-lookup"><span data-stu-id="23a8b-156">Get-AzureCertificate</span></span>](./Get-AzureCertificate.md)

[<span data-ttu-id="23a8b-157">Get-AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="23a8b-157">Get-AzureVMImage</span></span>](./Get-AzureVMImage.md)

[<span data-ttu-id="23a8b-158">새로운 AzureQuickVM</span><span class="sxs-lookup"><span data-stu-id="23a8b-158">New-AzureQuickVM</span></span>](./New-AzureQuickVM.md)

[<span data-ttu-id="23a8b-159">뉴욕</span><span class="sxs-lookup"><span data-stu-id="23a8b-159">New-AzureVM</span></span>](./New-AzureVM.md)

[<span data-ttu-id="23a8b-160">제거-AzureCertificate</span><span class="sxs-lookup"><span data-stu-id="23a8b-160">Remove-AzureCertificate</span></span>](./Remove-AzureCertificate.md)


