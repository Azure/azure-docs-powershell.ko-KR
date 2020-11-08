---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: A513B7CA-182E-46A2-8181-020C5DFC7DE9
online version: ''
schema: 2.0.0
ms.openlocfilehash: 316e7c182025171d2f1ba66ead1a0c0f5de120b1
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045504"
---
# <span data-ttu-id="5f10d-101">Remove-AzureVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="5f10d-101">Remove-AzureVMDiagnosticsExtension</span></span>

## <span data-ttu-id="5f10d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5f10d-102">SYNOPSIS</span></span>
<span data-ttu-id="5f10d-103">가상 컴퓨터에서 Azure Diagnostics 확장을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="5f10d-103">Removes the Azure Diagnostics extension from a virtual machine.</span></span>

## <span data-ttu-id="5f10d-104">구문과</span><span class="sxs-lookup"><span data-stu-id="5f10d-104">SYNTAX</span></span>

```
Remove-AzureVMDiagnosticsExtension -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="5f10d-105">설명은</span><span class="sxs-lookup"><span data-stu-id="5f10d-105">DESCRIPTION</span></span>
<span data-ttu-id="5f10d-106">**AzureVMDiagnosticsExtension** cmdlet은 가상 컴퓨터에서 Microsoft Azure 진단 확장을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="5f10d-106">The **Remove-AzureVMDiagnosticsExtension** cmdlet removes a Microsoft Azure Diagnostics extension from a virtual machine.</span></span>
<span data-ttu-id="5f10d-107">이 cmdlet의 출력을 **업데이트-add-azurevm** cmdlet에 전달 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="5f10d-107">You must pass the output of this cmdlet to the **Update-AzureVM** cmdlet.</span></span>

## <span data-ttu-id="5f10d-108">예제의</span><span class="sxs-lookup"><span data-stu-id="5f10d-108">EXAMPLES</span></span>

### <span data-ttu-id="5f10d-109">예제 1: 가상 머신에서 Azure Diagnostics 확장 제거</span><span class="sxs-lookup"><span data-stu-id="5f10d-109">Example 1: Remove the Azure Diagnostics extension from a virtual machine</span></span>
```
PS C:\> Remove-AzureVMDiagnosticsExtension -VM $VM | Update-AzureVM
```

<span data-ttu-id="5f10d-110">이 명령은 가상 컴퓨터에서 Azure Diagnostics 확장을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="5f10d-110">This command removes the Azure Diagnostics extension from a virtual machine.</span></span>

## <span data-ttu-id="5f10d-111">변수</span><span class="sxs-lookup"><span data-stu-id="5f10d-111">PARAMETERS</span></span>

### <span data-ttu-id="5f10d-112">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="5f10d-112">-InformationAction</span></span>
<span data-ttu-id="5f10d-113">이 cmdlet이 정보 이벤트에 응답 하는 방법을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5f10d-113">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="5f10d-114">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="5f10d-114">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="5f10d-115">하기로</span><span class="sxs-lookup"><span data-stu-id="5f10d-115">Continue</span></span>
- <span data-ttu-id="5f10d-116">숨기기</span><span class="sxs-lookup"><span data-stu-id="5f10d-116">Ignore</span></span>
- <span data-ttu-id="5f10d-117">Inquire</span><span class="sxs-lookup"><span data-stu-id="5f10d-117">Inquire</span></span>
- <span data-ttu-id="5f10d-118">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="5f10d-118">SilentlyContinue</span></span>
- <span data-ttu-id="5f10d-119">중지가</span><span class="sxs-lookup"><span data-stu-id="5f10d-119">Stop</span></span>
- <span data-ttu-id="5f10d-120">대기</span><span class="sxs-lookup"><span data-stu-id="5f10d-120">Suspend</span></span>

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

### <span data-ttu-id="5f10d-121">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="5f10d-121">-InformationVariable</span></span>
<span data-ttu-id="5f10d-122">정보 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5f10d-122">Specifies an information variable.</span></span>

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

### <span data-ttu-id="5f10d-123">-프로필</span><span class="sxs-lookup"><span data-stu-id="5f10d-123">-Profile</span></span>
<span data-ttu-id="5f10d-124">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5f10d-124">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="5f10d-125">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="5f10d-125">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="5f10d-126">-VM</span><span class="sxs-lookup"><span data-stu-id="5f10d-126">-VM</span></span>
<span data-ttu-id="5f10d-127">영구 가상 머신 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5f10d-127">Specifies the persistent virtual machine object.</span></span>

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

### <span data-ttu-id="5f10d-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5f10d-128">CommonParameters</span></span>
<span data-ttu-id="5f10d-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="5f10d-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5f10d-130">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5f10d-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5f10d-131">입력</span><span class="sxs-lookup"><span data-stu-id="5f10d-131">INPUTS</span></span>

## <span data-ttu-id="5f10d-132">출력</span><span class="sxs-lookup"><span data-stu-id="5f10d-132">OUTPUTS</span></span>

## <span data-ttu-id="5f10d-133">상속자</span><span class="sxs-lookup"><span data-stu-id="5f10d-133">NOTES</span></span>

## <span data-ttu-id="5f10d-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5f10d-134">RELATED LINKS</span></span>

[<span data-ttu-id="5f10d-135">Get-AzureVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="5f10d-135">Get-AzureVMDiagnosticsExtension</span></span>](./Get-AzureVMDiagnosticsExtension.md)

[<span data-ttu-id="5f10d-136">Set-AzureVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="5f10d-136">Set-AzureVMDiagnosticsExtension</span></span>](./Set-AzureVMDiagnosticsExtension.md)

[<span data-ttu-id="5f10d-137">업데이트-Add-azurevm</span><span class="sxs-lookup"><span data-stu-id="5f10d-137">Update-AzureVM</span></span>](./Update-AzureVM.md)


