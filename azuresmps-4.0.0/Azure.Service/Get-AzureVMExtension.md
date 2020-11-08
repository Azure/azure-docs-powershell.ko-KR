---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 7ED074F0-1E9E-40C2-A543-D19A49831DD3
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2f0b8ca9acfe5a62b002944bd44e11acfcd38ec1
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046533"
---
# <span data-ttu-id="b14f4-101">Get-AzureVMExtension</span><span class="sxs-lookup"><span data-stu-id="b14f4-101">Get-AzureVMExtension</span></span>

## <span data-ttu-id="b14f4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b14f4-102">SYNOPSIS</span></span>
<span data-ttu-id="b14f4-103">가상 컴퓨터에 적용 된 리소스 확장을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b14f4-103">Gets resource extensions applied to virtual machines.</span></span>

## <span data-ttu-id="b14f4-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b14f4-104">SYNTAX</span></span>

### <span data-ttu-id="b14f4-105">ListByReferenceName (기본값)</span><span class="sxs-lookup"><span data-stu-id="b14f4-105">ListByReferenceName (Default)</span></span>
```
Get-AzureVMExtension [[-ReferenceName] <String>] -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="b14f4-106">ListByExtensionName</span><span class="sxs-lookup"><span data-stu-id="b14f4-106">ListByExtensionName</span></span>
```
Get-AzureVMExtension [-ExtensionName] <String> [-Publisher] <String> [[-Version] <String>] -VM <IPersistentVM>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="b14f4-107">설명은</span><span class="sxs-lookup"><span data-stu-id="b14f4-107">DESCRIPTION</span></span>
<span data-ttu-id="b14f4-108">**Get-AzureVMExtension** cmdlet은 가상 컴퓨터에 적용 되는 리소스 확장을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b14f4-108">The **Get-AzureVMExtension** cmdlet gets resource extensions applied to virtual machines.</span></span>

## <span data-ttu-id="b14f4-109">예제의</span><span class="sxs-lookup"><span data-stu-id="b14f4-109">EXAMPLES</span></span>

### <span data-ttu-id="b14f4-110">예제 1: 가상 컴퓨터에 적용 된 리소스 확장 가져오기</span><span class="sxs-lookup"><span data-stu-id="b14f4-110">Example 1: Get the resource extensions applied to a virtual machine</span></span>
```
PS C:\> Get-AzureVM -ServiceName $SVC -Name $VM | Get-AzureVMExtension;
```

<span data-ttu-id="b14f4-111">이 명령은 $VM 변수에 저장 되는 지정 된 가상 컴퓨터에 적용 된 리소스 확장을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b14f4-111">This command gets the resource extensions applied to the specified virtual machine as stored in the variable $VM.</span></span>

## <span data-ttu-id="b14f4-112">변수</span><span class="sxs-lookup"><span data-stu-id="b14f4-112">PARAMETERS</span></span>

### <span data-ttu-id="b14f4-113">-ExtensionName</span><span class="sxs-lookup"><span data-stu-id="b14f4-113">-ExtensionName</span></span>
<span data-ttu-id="b14f4-114">가상 컴퓨터 확장 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b14f4-114">Specifies the virtual machine extension name.</span></span>

```yaml
Type: String
Parameter Sets: ListByExtensionName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b14f4-115">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="b14f4-115">-InformationAction</span></span>
<span data-ttu-id="b14f4-116">이 cmdlet이 정보 이벤트에 응답 하는 방법을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b14f4-116">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="b14f4-117">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="b14f4-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="b14f4-118">하기로</span><span class="sxs-lookup"><span data-stu-id="b14f4-118">Continue</span></span>
- <span data-ttu-id="b14f4-119">숨기기</span><span class="sxs-lookup"><span data-stu-id="b14f4-119">Ignore</span></span>
- <span data-ttu-id="b14f4-120">Inquire</span><span class="sxs-lookup"><span data-stu-id="b14f4-120">Inquire</span></span>
- <span data-ttu-id="b14f4-121">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="b14f4-121">SilentlyContinue</span></span>
- <span data-ttu-id="b14f4-122">중지가</span><span class="sxs-lookup"><span data-stu-id="b14f4-122">Stop</span></span>
- <span data-ttu-id="b14f4-123">대기</span><span class="sxs-lookup"><span data-stu-id="b14f4-123">Suspend</span></span>

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

### <span data-ttu-id="b14f4-124">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="b14f4-124">-InformationVariable</span></span>
<span data-ttu-id="b14f4-125">정보 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b14f4-125">Specifies an information variable.</span></span>

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

### <span data-ttu-id="b14f4-126">-프로필</span><span class="sxs-lookup"><span data-stu-id="b14f4-126">-Profile</span></span>
<span data-ttu-id="b14f4-127">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b14f4-127">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="b14f4-128">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="b14f4-128">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="b14f4-129">-Publisher</span><span class="sxs-lookup"><span data-stu-id="b14f4-129">-Publisher</span></span>
<span data-ttu-id="b14f4-130">확장의 게시자를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b14f4-130">Specifies the publisher of the extension.</span></span>

```yaml
Type: String
Parameter Sets: ListByExtensionName
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b14f4-131">-ReferenceName</span><span class="sxs-lookup"><span data-stu-id="b14f4-131">-ReferenceName</span></span>
<span data-ttu-id="b14f4-132">확장의 참조 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b14f4-132">Specifies the reference name of the extension.</span></span>

```yaml
Type: String
Parameter Sets: ListByReferenceName
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b14f4-133">-버전</span><span class="sxs-lookup"><span data-stu-id="b14f4-133">-Version</span></span>
<span data-ttu-id="b14f4-134">확장의 버전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b14f4-134">Specifies the version of the extension.</span></span>

```yaml
Type: String
Parameter Sets: ListByExtensionName
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b14f4-135">-VM</span><span class="sxs-lookup"><span data-stu-id="b14f4-135">-VM</span></span>
<span data-ttu-id="b14f4-136">영구 가상 머신 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b14f4-136">Specifies the persistent virtual machine object.</span></span>

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

### <span data-ttu-id="b14f4-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b14f4-137">CommonParameters</span></span>
<span data-ttu-id="b14f4-138">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b14f4-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b14f4-139">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b14f4-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b14f4-140">입력</span><span class="sxs-lookup"><span data-stu-id="b14f4-140">INPUTS</span></span>

## <span data-ttu-id="b14f4-141">출력</span><span class="sxs-lookup"><span data-stu-id="b14f4-141">OUTPUTS</span></span>

## <span data-ttu-id="b14f4-142">상속자</span><span class="sxs-lookup"><span data-stu-id="b14f4-142">NOTES</span></span>

## <span data-ttu-id="b14f4-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b14f4-143">RELATED LINKS</span></span>

[<span data-ttu-id="b14f4-144">제거-AzureVMExtension</span><span class="sxs-lookup"><span data-stu-id="b14f4-144">Remove-AzureVMExtension</span></span>](./Remove-AzureVMExtension.md)

[<span data-ttu-id="b14f4-145">Set-AzureVMExtension</span><span class="sxs-lookup"><span data-stu-id="b14f4-145">Set-AzureVMExtension</span></span>](./Set-AzureVMExtension.md)


