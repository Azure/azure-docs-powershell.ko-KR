---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 4E3D405D-69FB-42C2-8A5B-BDBD27B63088
online version: ''
schema: 2.0.0
ms.openlocfilehash: 503c2e0a076be3f31b6435a30dc658af9b45835a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046167"
---
# <span data-ttu-id="0f771-101">Remove-AzureCertificate</span><span class="sxs-lookup"><span data-stu-id="0f771-101">Remove-AzureCertificate</span></span>

## <span data-ttu-id="0f771-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0f771-102">SYNOPSIS</span></span>
<span data-ttu-id="0f771-103">Azure 서비스에서 인증서를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="0f771-103">Removes a certificate from an Azure service.</span></span>

## <span data-ttu-id="0f771-104">구문과</span><span class="sxs-lookup"><span data-stu-id="0f771-104">SYNTAX</span></span>

```
Remove-AzureCertificate [-ServiceName] <String> [-ThumbprintAlgorithm] <String> [-Thumbprint] <String>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="0f771-105">설명은</span><span class="sxs-lookup"><span data-stu-id="0f771-105">DESCRIPTION</span></span>
<span data-ttu-id="0f771-106">**제거-AzureCertificate** Cmdlet은 Azure 서비스에서 인증서를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="0f771-106">The **Remove-AzureCertificate** cmdlet removes a certificate from an Azure service.</span></span>

## <span data-ttu-id="0f771-107">예제의</span><span class="sxs-lookup"><span data-stu-id="0f771-107">EXAMPLES</span></span>

### <span data-ttu-id="0f771-108">예제 1: 서비스에서 인증서 제거</span><span class="sxs-lookup"><span data-stu-id="0f771-108">Example 1: Remove a certificate from a service</span></span>
```
PS C:\> Remove-AzureCertificate -ServiceName "ContosoService" -Thumbprint '5383CE0343CB6563281CA97C1D4D712209CFFA97'
```

<span data-ttu-id="0f771-109">이 명령은 클라우드 서비스에서 지정 된 지문이 있는 인증서 개체를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="0f771-109">This command removes the certificate object that has the specified thumbprint from the cloud service.</span></span>

### <span data-ttu-id="0f771-110">예제 2: 서비스에서 모든 인증서 제거</span><span class="sxs-lookup"><span data-stu-id="0f771-110">Example 2: Remove all certificates from a service</span></span>
```
PS C:\> Get-AzureCertificate -ServiceName "ContosoService" | Remove-AzureCertificate
```

<span data-ttu-id="0f771-111">이 명령은 **AzureCertificate** cmdlet을 사용 하 여 ContosoService 이라는 서비스에서 모든 인증서를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="0f771-111">This command gets all the certificates from the service named ContosoService by using the **Get-AzureCertificate** cmdlet.</span></span>
<span data-ttu-id="0f771-112">이 명령은 파이프라인 연산자를 사용 하 여 각 인증서를 현재 cmdlet에 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="0f771-112">The command passes each certificate to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="0f771-113">해당 cmdlet은 클라우드 서비스에서 각 인증서를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="0f771-113">That cmdlet removes each certificate from the cloud service.</span></span>

### <span data-ttu-id="0f771-114">예제 3: 특정 손도장 알고리즘을 사용 하는 서비스에서 모든 인증서 제거</span><span class="sxs-lookup"><span data-stu-id="0f771-114">Example 3: Remove all certificates from a service that use a specific thumbprint algorithm</span></span>
```
PS C:\> Get-AzureCertificate -ServiceName "ContosoService" -ThumbprintAlgorithm "sha1" | Remove-AzureCertificate
```

<span data-ttu-id="0f771-115">이 명령은 sha1 손도장 알고리즘을 사용 하는 ContosoService 이라는 서비스에서 모든 인증서를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="0f771-115">This command gets all the certificates from the service named ContosoService that use the sha1 thumbprint algorithm.</span></span>
<span data-ttu-id="0f771-116">명령이 각 인증서를 현재 cmdlet에 전달 하 여 각 인증서를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="0f771-116">The command passes each certificate to the current cmdlet, which removes each certificate.</span></span>

## <span data-ttu-id="0f771-117">변수</span><span class="sxs-lookup"><span data-stu-id="0f771-117">PARAMETERS</span></span>

### <span data-ttu-id="0f771-118">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="0f771-118">-InformationAction</span></span>
<span data-ttu-id="0f771-119">이 cmdlet이 정보 이벤트에 응답 하는 방법을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0f771-119">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="0f771-120">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="0f771-120">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="0f771-121">하기로</span><span class="sxs-lookup"><span data-stu-id="0f771-121">Continue</span></span>
- <span data-ttu-id="0f771-122">숨기기</span><span class="sxs-lookup"><span data-stu-id="0f771-122">Ignore</span></span>
- <span data-ttu-id="0f771-123">Inquire</span><span class="sxs-lookup"><span data-stu-id="0f771-123">Inquire</span></span>
- <span data-ttu-id="0f771-124">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="0f771-124">SilentlyContinue</span></span>
- <span data-ttu-id="0f771-125">중지가</span><span class="sxs-lookup"><span data-stu-id="0f771-125">Stop</span></span>
- <span data-ttu-id="0f771-126">대기</span><span class="sxs-lookup"><span data-stu-id="0f771-126">Suspend</span></span>

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

### <span data-ttu-id="0f771-127">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="0f771-127">-InformationVariable</span></span>
<span data-ttu-id="0f771-128">정보 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0f771-128">Specifies an information variable.</span></span>

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

### <span data-ttu-id="0f771-129">-프로필</span><span class="sxs-lookup"><span data-stu-id="0f771-129">-Profile</span></span>
<span data-ttu-id="0f771-130">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0f771-130">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="0f771-131">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="0f771-131">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="0f771-132">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="0f771-132">-ServiceName</span></span>
<span data-ttu-id="0f771-133">이 cmdlet에서 인증서를 제거 하는 Azure 서비스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0f771-133">Specifies the name of the Azure service from which this cmdlet removes a certificate.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0f771-134">-지문</span><span class="sxs-lookup"><span data-stu-id="0f771-134">-Thumbprint</span></span>
<span data-ttu-id="0f771-135">이 cmdlet이 제거 하는 인증서의 지문을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0f771-135">Specifies the thumbprint of the certificate that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0f771-136">-ThumbprintAlgorithm</span><span class="sxs-lookup"><span data-stu-id="0f771-136">-ThumbprintAlgorithm</span></span>
<span data-ttu-id="0f771-137">인증서 지문을 만드는 데 사용 되는 알고리즘을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0f771-137">Specifies the algorithm that is used to create the certificate thumbprint.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0f771-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f771-138">CommonParameters</span></span>
<span data-ttu-id="0f771-139">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="0f771-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f771-140">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0f771-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f771-141">입력</span><span class="sxs-lookup"><span data-stu-id="0f771-141">INPUTS</span></span>

## <span data-ttu-id="0f771-142">출력</span><span class="sxs-lookup"><span data-stu-id="0f771-142">OUTPUTS</span></span>

### <span data-ttu-id="0f771-143">ManagementOperationContext</span><span class="sxs-lookup"><span data-stu-id="0f771-143">ManagementOperationContext</span></span>

## <span data-ttu-id="0f771-144">상속자</span><span class="sxs-lookup"><span data-stu-id="0f771-144">NOTES</span></span>

## <span data-ttu-id="0f771-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0f771-145">RELATED LINKS</span></span>

[<span data-ttu-id="0f771-146">추가-AzureCertificate</span><span class="sxs-lookup"><span data-stu-id="0f771-146">Add-AzureCertificate</span></span>](./Add-AzureCertificate.md)

[<span data-ttu-id="0f771-147">Get-AzureCertificate</span><span class="sxs-lookup"><span data-stu-id="0f771-147">Get-AzureCertificate</span></span>](./Get-AzureCertificate.md)

[<span data-ttu-id="0f771-148">새로운 AzureCertificateSetting</span><span class="sxs-lookup"><span data-stu-id="0f771-148">New-AzureCertificateSetting</span></span>](./New-AzureCertificateSetting.md)


