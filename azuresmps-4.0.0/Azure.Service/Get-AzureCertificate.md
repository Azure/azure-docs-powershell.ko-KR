---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 7BEFA810-685C-4553-BED8-4CD6BCF8A5FE
online version: ''
schema: 2.0.0
ms.openlocfilehash: d88784e5d4fdd153700bd3879262198e5dd3807a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046356"
---
# <span data-ttu-id="58ecb-101">Get-AzureCertificate</span><span class="sxs-lookup"><span data-stu-id="58ecb-101">Get-AzureCertificate</span></span>

## <span data-ttu-id="58ecb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="58ecb-102">SYNOPSIS</span></span>
<span data-ttu-id="58ecb-103">Azure 서비스에서 인증서 개체를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="58ecb-103">Gets a certificate object from an Azure service.</span></span>

## <span data-ttu-id="58ecb-104">구문과</span><span class="sxs-lookup"><span data-stu-id="58ecb-104">SYNTAX</span></span>

```
Get-AzureCertificate [-ServiceName] <String> [-ThumbprintAlgorithm <String>] [-Thumbprint <String>]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="58ecb-105">설명은</span><span class="sxs-lookup"><span data-stu-id="58ecb-105">DESCRIPTION</span></span>
<span data-ttu-id="58ecb-106">**Get-AzureCertificate** Cmdlet은 Azure 서비스에서 인증서 개체를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="58ecb-106">The **Get-AzureCertificate** cmdlet gets a certificate object from an Azure service.</span></span>

## <span data-ttu-id="58ecb-107">예제의</span><span class="sxs-lookup"><span data-stu-id="58ecb-107">EXAMPLES</span></span>

### <span data-ttu-id="58ecb-108">예제 1: 서비스에서 인증서 가져오기</span><span class="sxs-lookup"><span data-stu-id="58ecb-108">Example 1: Get certificates from a service</span></span>
```
PS C:\> $AzureCert = Get-AzureCertificate -ServiceName "ContosoService"
```

<span data-ttu-id="58ecb-109">이 명령은 ContosoService 이라는 서비스에서 인증서 개체를 가져온 다음이를 $AzureCert 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="58ecb-109">This command gets certificate objects from the service named ContosoService, and then stores them in the $AzureCert variable.</span></span>

### <span data-ttu-id="58ecb-110">예제 2: 서비스에서 인증서 가져오기</span><span class="sxs-lookup"><span data-stu-id="58ecb-110">Example 2: Get a certificate from a service</span></span>
```
PS C:\> $AzureCert = Get-AzureCertificate -ServiceName "ContosoService" -Thumbprint '5383CE0343CB6563281CA97C1D4D712209CFFA97'
```

<span data-ttu-id="58ecb-111">이 명령은 ContosoService 이라는 서비스에서 지정 된 손도장으로 식별 되는 인증서 개체를 가져온 다음이를 $AzureCert 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="58ecb-111">This command gets the certificate object identified by the specified thumbprint from the service named ContosoService, and then stores it in the $AzureCert variable.</span></span>

## <span data-ttu-id="58ecb-112">변수</span><span class="sxs-lookup"><span data-stu-id="58ecb-112">PARAMETERS</span></span>

### <span data-ttu-id="58ecb-113">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="58ecb-113">-InformationAction</span></span>
<span data-ttu-id="58ecb-114">이 cmdlet이 정보 이벤트에 응답 하는 방법을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="58ecb-114">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="58ecb-115">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="58ecb-115">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="58ecb-116">하기로</span><span class="sxs-lookup"><span data-stu-id="58ecb-116">Continue</span></span>
- <span data-ttu-id="58ecb-117">숨기기</span><span class="sxs-lookup"><span data-stu-id="58ecb-117">Ignore</span></span>
- <span data-ttu-id="58ecb-118">Inquire</span><span class="sxs-lookup"><span data-stu-id="58ecb-118">Inquire</span></span>
- <span data-ttu-id="58ecb-119">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="58ecb-119">SilentlyContinue</span></span>
- <span data-ttu-id="58ecb-120">중지가</span><span class="sxs-lookup"><span data-stu-id="58ecb-120">Stop</span></span>
- <span data-ttu-id="58ecb-121">대기</span><span class="sxs-lookup"><span data-stu-id="58ecb-121">Suspend</span></span>

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

### <span data-ttu-id="58ecb-122">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="58ecb-122">-InformationVariable</span></span>
<span data-ttu-id="58ecb-123">정보 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="58ecb-123">Specifies an information variable.</span></span>

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

### <span data-ttu-id="58ecb-124">-프로필</span><span class="sxs-lookup"><span data-stu-id="58ecb-124">-Profile</span></span>
<span data-ttu-id="58ecb-125">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="58ecb-125">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="58ecb-126">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="58ecb-126">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="58ecb-127">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="58ecb-127">-ServiceName</span></span>
<span data-ttu-id="58ecb-128">이 cmdlet에서 인증서를 가져오는 Azure 서비스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="58ecb-128">Specifies the name of the Azure service from which this cmdlet gets a certificate.</span></span>

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

### <span data-ttu-id="58ecb-129">-지문</span><span class="sxs-lookup"><span data-stu-id="58ecb-129">-Thumbprint</span></span>
<span data-ttu-id="58ecb-130">이 cmdlet이 가져오는 인증서의 지문을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="58ecb-130">Specifies the thumbprint of the certificate that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="58ecb-131">-ThumbprintAlgorithm</span><span class="sxs-lookup"><span data-stu-id="58ecb-131">-ThumbprintAlgorithm</span></span>
<span data-ttu-id="58ecb-132">인증서 지문을 만드는 데 사용 되는 알고리즘을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="58ecb-132">Specifies the algorithm that is used to create the certificate thumbprint.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="58ecb-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58ecb-133">CommonParameters</span></span>
<span data-ttu-id="58ecb-134">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="58ecb-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58ecb-135">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="58ecb-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58ecb-136">입력</span><span class="sxs-lookup"><span data-stu-id="58ecb-136">INPUTS</span></span>

## <span data-ttu-id="58ecb-137">출력</span><span class="sxs-lookup"><span data-stu-id="58ecb-137">OUTPUTS</span></span>

### <span data-ttu-id="58ecb-138">CertificateContext</span><span class="sxs-lookup"><span data-stu-id="58ecb-138">CertificateContext</span></span>

## <span data-ttu-id="58ecb-139">상속자</span><span class="sxs-lookup"><span data-stu-id="58ecb-139">NOTES</span></span>

## <span data-ttu-id="58ecb-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="58ecb-140">RELATED LINKS</span></span>

[<span data-ttu-id="58ecb-141">추가-AzureCertificate</span><span class="sxs-lookup"><span data-stu-id="58ecb-141">Add-AzureCertificate</span></span>](./Add-AzureCertificate.md)

[<span data-ttu-id="58ecb-142">새로운 AzureCertificateSetting</span><span class="sxs-lookup"><span data-stu-id="58ecb-142">New-AzureCertificateSetting</span></span>](./New-AzureCertificateSetting.md)

[<span data-ttu-id="58ecb-143">제거-AzureCertificate</span><span class="sxs-lookup"><span data-stu-id="58ecb-143">Remove-AzureCertificate</span></span>](./Remove-AzureCertificate.md)


