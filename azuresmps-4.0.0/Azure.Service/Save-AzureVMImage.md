---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 9A1CE31E-0158-441E-BC2D-B5D21C9D9421
online version: ''
schema: 2.0.0
ms.openlocfilehash: a956aa7eaf383b0cf5cdb20b39d2f6b54e292f92
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045451"
---
# <span data-ttu-id="d2e27-101">Save-AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="d2e27-101">Save-AzureVMImage</span></span>

## <span data-ttu-id="d2e27-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d2e27-102">SYNOPSIS</span></span>
<span data-ttu-id="d2e27-103">중지 된 Azure 가상 컴퓨터의 이미지를 캡처하여 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="d2e27-103">Captures and saves the image of a stopped Azure virtual machine.</span></span>

## <span data-ttu-id="d2e27-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d2e27-104">SYNTAX</span></span>

```
Save-AzureVMImage [-ServiceName] <String> [-Name] <String> [-ImageName] <String> [[-ImageLabel] <String>]
 [[-OSState] <String>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="d2e27-105">설명은</span><span class="sxs-lookup"><span data-stu-id="d2e27-105">DESCRIPTION</span></span>
<span data-ttu-id="d2e27-106">**AzureVMImage** cmdlet은 중지 된 Azure 가상 컴퓨터의 이미지를 캡처하고 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="d2e27-106">The **Save-AzureVMImage** cmdlet captures and saves the image of a stopped Azure virtual machine.</span></span>
<span data-ttu-id="d2e27-107">Windows 가상 컴퓨터의 경우 Sysprep 도구를 실행 하 여 캡처 전에 이미지를 준비 합니다.</span><span class="sxs-lookup"><span data-stu-id="d2e27-107">For Windows virtual machines, run the Sysprep tool to prepare the image before it is captured.</span></span>
<span data-ttu-id="d2e27-108">이미지가 캡처되면 가상 컴퓨터가 삭제 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d2e27-108">After the image is captured, the virtual machine is deleted.</span></span>

## <span data-ttu-id="d2e27-109">예제의</span><span class="sxs-lookup"><span data-stu-id="d2e27-109">EXAMPLES</span></span>

### <span data-ttu-id="d2e27-110">예제 1: 기존 가상 컴퓨터를 저장 한 다음 배포에서 삭제</span><span class="sxs-lookup"><span data-stu-id="d2e27-110">Example 1: Save an existing virtual machine and then delete it from a deployment</span></span>
```
PS C:\> Save-AzureVMImage -ServiceName "MyService" -Name "MyVM" -NewImageName "MyBaseImage" -NewImageLabel "MyBaseVM"
```

<span data-ttu-id="d2e27-111">이 명령은 기존 가상 컴퓨터를 캡처하여 배포에서 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="d2e27-111">This command captures an existing virtual machine and deletes it from the deployment.</span></span>

## <span data-ttu-id="d2e27-112">변수</span><span class="sxs-lookup"><span data-stu-id="d2e27-112">PARAMETERS</span></span>

### <span data-ttu-id="d2e27-113">-ImageLabel</span><span class="sxs-lookup"><span data-stu-id="d2e27-113">-ImageLabel</span></span>
<span data-ttu-id="d2e27-114">가상 컴퓨터 이미지의 레이블을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d2e27-114">Specifies the label of the virtual machine image.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: NewImageLabel

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d2e27-115">-ImageName</span><span class="sxs-lookup"><span data-stu-id="d2e27-115">-ImageName</span></span>
<span data-ttu-id="d2e27-116">가상 컴퓨터 이미지의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d2e27-116">Specifies the name of the virtual machine image.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: NewImageName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d2e27-117">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="d2e27-117">-InformationAction</span></span>
<span data-ttu-id="d2e27-118">이 cmdlet이 정보 이벤트에 응답 하는 방법을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d2e27-118">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="d2e27-119">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="d2e27-119">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="d2e27-120">하기로</span><span class="sxs-lookup"><span data-stu-id="d2e27-120">Continue</span></span>
- <span data-ttu-id="d2e27-121">숨기기</span><span class="sxs-lookup"><span data-stu-id="d2e27-121">Ignore</span></span>
- <span data-ttu-id="d2e27-122">Inquire</span><span class="sxs-lookup"><span data-stu-id="d2e27-122">Inquire</span></span>
- <span data-ttu-id="d2e27-123">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="d2e27-123">SilentlyContinue</span></span>
- <span data-ttu-id="d2e27-124">중지가</span><span class="sxs-lookup"><span data-stu-id="d2e27-124">Stop</span></span>
- <span data-ttu-id="d2e27-125">대기</span><span class="sxs-lookup"><span data-stu-id="d2e27-125">Suspend</span></span>

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

### <span data-ttu-id="d2e27-126">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="d2e27-126">-InformationVariable</span></span>
<span data-ttu-id="d2e27-127">정보 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d2e27-127">Specifies an information variable.</span></span>

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

### <span data-ttu-id="d2e27-128">-이름</span><span class="sxs-lookup"><span data-stu-id="d2e27-128">-Name</span></span>
<span data-ttu-id="d2e27-129">원본 가상 컴퓨터의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d2e27-129">Specifies the name of the source virtual machine.</span></span>

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

### <span data-ttu-id="d2e27-130">-OSState</span><span class="sxs-lookup"><span data-stu-id="d2e27-130">-OSState</span></span>
<span data-ttu-id="d2e27-131">가상 컴퓨터 이미지의 운영 체제 상태를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d2e27-131">Specifies the operation system state for the virtual machine image.</span></span>
<span data-ttu-id="d2e27-132">Azure에 대 한 가상 컴퓨터 이미지를 캡처하려면이 매개 변수를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="d2e27-132">Use this parameter if you intend to capture a virtual machine image to Azure.</span></span>

<span data-ttu-id="d2e27-133">유효한 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="d2e27-133">Valid values are:</span></span>

- <span data-ttu-id="d2e27-134">Generalize</span><span class="sxs-lookup"><span data-stu-id="d2e27-134">Generalized</span></span>
- <span data-ttu-id="d2e27-135">위한</span><span class="sxs-lookup"><span data-stu-id="d2e27-135">Specialized</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d2e27-136">-프로필</span><span class="sxs-lookup"><span data-stu-id="d2e27-136">-Profile</span></span>
<span data-ttu-id="d2e27-137">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d2e27-137">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="d2e27-138">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="d2e27-138">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="d2e27-139">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="d2e27-139">-ServiceName</span></span>
<span data-ttu-id="d2e27-140">Azure 서비스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d2e27-140">Specifies the name of the Azure service.</span></span>

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

### <span data-ttu-id="d2e27-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2e27-141">CommonParameters</span></span>
<span data-ttu-id="d2e27-142">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d2e27-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2e27-143">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d2e27-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2e27-144">입력</span><span class="sxs-lookup"><span data-stu-id="d2e27-144">INPUTS</span></span>

## <span data-ttu-id="d2e27-145">출력</span><span class="sxs-lookup"><span data-stu-id="d2e27-145">OUTPUTS</span></span>

## <span data-ttu-id="d2e27-146">상속자</span><span class="sxs-lookup"><span data-stu-id="d2e27-146">NOTES</span></span>

## <span data-ttu-id="d2e27-147">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d2e27-147">RELATED LINKS</span></span>

[<span data-ttu-id="d2e27-148">추가-AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="d2e27-148">Add-AzureVMImage</span></span>](./Add-AzureVMImage.md)

[<span data-ttu-id="d2e27-149">Get-AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="d2e27-149">Get-AzureVMImage</span></span>](./Get-AzureVMImage.md)

[<span data-ttu-id="d2e27-150">제거-AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="d2e27-150">Remove-AzureVMImage</span></span>](./Remove-AzureVMImage.md)

[<span data-ttu-id="d2e27-151">업데이트-AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="d2e27-151">Update-AzureVMImage</span></span>](./Update-AzureVMImage.md)


