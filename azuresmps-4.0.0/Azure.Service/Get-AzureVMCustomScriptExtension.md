---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: DBB8EC31-877C-4DB1-8197-CA7A4148AE06
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2f8767c9477db41251eb4732a2eb96d8dd782c20
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045531"
---
# <span data-ttu-id="f60a8-101">Get-AzureVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="f60a8-101">Get-AzureVMCustomScriptExtension</span></span>

## <span data-ttu-id="f60a8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f60a8-102">SYNOPSIS</span></span>
<span data-ttu-id="f60a8-103">Azure virtual machine 사용자 지정 스크립트 확장에서 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f60a8-103">Gets information from an Azure virtual machine custom script extension.</span></span>

## <span data-ttu-id="f60a8-104">구문과</span><span class="sxs-lookup"><span data-stu-id="f60a8-104">SYNTAX</span></span>

```
Get-AzureVMCustomScriptExtension -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="f60a8-105">설명은</span><span class="sxs-lookup"><span data-stu-id="f60a8-105">DESCRIPTION</span></span>
<span data-ttu-id="f60a8-106">**AzureVMCustomScriptExtension** Cmdlet은 Azure virtual machine 사용자 지정 스크립트 확장에서 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f60a8-106">The **Get-AzureVMCustomScriptExtension** cmdlet gets information from an Azure virtual machine custom script extension.</span></span>

## <span data-ttu-id="f60a8-107">예제의</span><span class="sxs-lookup"><span data-stu-id="f60a8-107">EXAMPLES</span></span>

### <span data-ttu-id="f60a8-108">예제 1: Azure 가상 컴퓨터 스크립트 확장 가져오기</span><span class="sxs-lookup"><span data-stu-id="f60a8-108">Example 1: Get an Azure virtual machine script extension</span></span>
```
PS C:\> Get-AzureVMCustomScriptExtension -VM $VM;
```

<span data-ttu-id="f60a8-109">이 명령은 변수 $VM에 저장 된 Azure 가상 컴퓨터 스크립트 확장을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f60a8-109">This command gets an Azure virtual machine script extension stored in the variable $VM.</span></span>

## <span data-ttu-id="f60a8-110">변수</span><span class="sxs-lookup"><span data-stu-id="f60a8-110">PARAMETERS</span></span>

### <span data-ttu-id="f60a8-111">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="f60a8-111">-InformationAction</span></span>
<span data-ttu-id="f60a8-112">이 cmdlet이 정보 이벤트에 응답 하는 방법을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f60a8-112">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="f60a8-113">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="f60a8-113">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="f60a8-114">하기로</span><span class="sxs-lookup"><span data-stu-id="f60a8-114">Continue</span></span>
- <span data-ttu-id="f60a8-115">숨기기</span><span class="sxs-lookup"><span data-stu-id="f60a8-115">Ignore</span></span>
- <span data-ttu-id="f60a8-116">Inquire</span><span class="sxs-lookup"><span data-stu-id="f60a8-116">Inquire</span></span>
- <span data-ttu-id="f60a8-117">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="f60a8-117">SilentlyContinue</span></span>
- <span data-ttu-id="f60a8-118">중지가</span><span class="sxs-lookup"><span data-stu-id="f60a8-118">Stop</span></span>
- <span data-ttu-id="f60a8-119">대기</span><span class="sxs-lookup"><span data-stu-id="f60a8-119">Suspend</span></span>

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

### <span data-ttu-id="f60a8-120">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="f60a8-120">-InformationVariable</span></span>
<span data-ttu-id="f60a8-121">정보 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f60a8-121">Specifies an information variable.</span></span>

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

### <span data-ttu-id="f60a8-122">-프로필</span><span class="sxs-lookup"><span data-stu-id="f60a8-122">-Profile</span></span>
<span data-ttu-id="f60a8-123">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f60a8-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="f60a8-124">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="f60a8-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="f60a8-125">-VM</span><span class="sxs-lookup"><span data-stu-id="f60a8-125">-VM</span></span>
<span data-ttu-id="f60a8-126">영구 가상 머신 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f60a8-126">Specifies the persistent virtual machine object.</span></span>

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

### <span data-ttu-id="f60a8-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f60a8-127">CommonParameters</span></span>
<span data-ttu-id="f60a8-128">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f60a8-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f60a8-129">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f60a8-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f60a8-130">입력</span><span class="sxs-lookup"><span data-stu-id="f60a8-130">INPUTS</span></span>

## <span data-ttu-id="f60a8-131">출력</span><span class="sxs-lookup"><span data-stu-id="f60a8-131">OUTPUTS</span></span>

## <span data-ttu-id="f60a8-132">상속자</span><span class="sxs-lookup"><span data-stu-id="f60a8-132">NOTES</span></span>

## <span data-ttu-id="f60a8-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f60a8-133">RELATED LINKS</span></span>

[<span data-ttu-id="f60a8-134">제거-AzureVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="f60a8-134">Remove-AzureVMCustomScriptExtension</span></span>](./Remove-AzureVMCustomScriptExtension.md)

[<span data-ttu-id="f60a8-135">Set-AzureVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="f60a8-135">Set-AzureVMCustomScriptExtension</span></span>](./Set-AzureVMCustomScriptExtension.md)


