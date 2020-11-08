---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 40AE50AA-6807-4481-8B77-A038914D462E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7a4c6997a7ae70a72a21800cce1d4f5f32475a85
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046447"
---
# <span data-ttu-id="ec912-101">Remove-AzureVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="ec912-101">Remove-AzureVMDscExtension</span></span>

## <span data-ttu-id="ec912-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ec912-102">SYNOPSIS</span></span>
<span data-ttu-id="ec912-103">가상 컴퓨터에서 Azure DSC 확장을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="ec912-103">Removes an Azure DSC extension from a virtual machine.</span></span>

## <span data-ttu-id="ec912-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ec912-104">SYNTAX</span></span>

```
Remove-AzureVMDscExtension -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ec912-105">설명은</span><span class="sxs-lookup"><span data-stu-id="ec912-105">DESCRIPTION</span></span>
<span data-ttu-id="ec912-106">**AzureVMDscExtension** cmdlet은 가상 컴퓨터에서 Azure DSC 확장을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="ec912-106">The **Remove-AzureVMDscExtension** cmdlet removes an Azure DSC extension from a virtual machine.</span></span>
<span data-ttu-id="ec912-107">이 cmdlet의 출력을 **업데이트-add-azurevm** cmdlet으로 파이프 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="ec912-107">The output of this cmdlet needs to be piped to the **Update-AzureVM** cmdlet.</span></span>

## <span data-ttu-id="ec912-108">예제의</span><span class="sxs-lookup"><span data-stu-id="ec912-108">EXAMPLES</span></span>

### <span data-ttu-id="ec912-109">예제 1: 가상 컴퓨터에서 DSC 확장 제거</span><span class="sxs-lookup"><span data-stu-id="ec912-109">Example 1: Remove a DSC extension from a virtual machine</span></span>
```
PS C:\> Remove-AzureVMDscExtension -VM $VM | Update-AzureVM
```

<span data-ttu-id="ec912-110">이 명령은 가상 컴퓨터에서 Azure DSC 확장을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="ec912-110">This command removes an Azure DSC extension from a virtual machine.</span></span>

## <span data-ttu-id="ec912-111">변수</span><span class="sxs-lookup"><span data-stu-id="ec912-111">PARAMETERS</span></span>

### <span data-ttu-id="ec912-112">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="ec912-112">-InformationAction</span></span>
<span data-ttu-id="ec912-113">이 cmdlet이 정보 이벤트에 응답 하는 방법을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ec912-113">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="ec912-114">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="ec912-114">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="ec912-115">하기로</span><span class="sxs-lookup"><span data-stu-id="ec912-115">Continue</span></span>
- <span data-ttu-id="ec912-116">숨기기</span><span class="sxs-lookup"><span data-stu-id="ec912-116">Ignore</span></span>
- <span data-ttu-id="ec912-117">Inquire</span><span class="sxs-lookup"><span data-stu-id="ec912-117">Inquire</span></span>
- <span data-ttu-id="ec912-118">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="ec912-118">SilentlyContinue</span></span>
- <span data-ttu-id="ec912-119">중지가</span><span class="sxs-lookup"><span data-stu-id="ec912-119">Stop</span></span>
- <span data-ttu-id="ec912-120">대기</span><span class="sxs-lookup"><span data-stu-id="ec912-120">Suspend</span></span>

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

### <span data-ttu-id="ec912-121">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="ec912-121">-InformationVariable</span></span>
<span data-ttu-id="ec912-122">정보 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ec912-122">Specifies an information variable.</span></span>

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

### <span data-ttu-id="ec912-123">-프로필</span><span class="sxs-lookup"><span data-stu-id="ec912-123">-Profile</span></span>
<span data-ttu-id="ec912-124">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ec912-124">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="ec912-125">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="ec912-125">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="ec912-126">-VM</span><span class="sxs-lookup"><span data-stu-id="ec912-126">-VM</span></span>
<span data-ttu-id="ec912-127">영구 가상 머신 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ec912-127">Specifies the persistent virtual machine object.</span></span>

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

### <span data-ttu-id="ec912-128">-확인</span><span class="sxs-lookup"><span data-stu-id="ec912-128">-Confirm</span></span>
<span data-ttu-id="ec912-129">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="ec912-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec912-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ec912-130">-WhatIf</span></span>
<span data-ttu-id="ec912-131">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="ec912-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ec912-132">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ec912-132">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec912-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec912-133">CommonParameters</span></span>
<span data-ttu-id="ec912-134">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ec912-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec912-135">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ec912-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec912-136">입력</span><span class="sxs-lookup"><span data-stu-id="ec912-136">INPUTS</span></span>

## <span data-ttu-id="ec912-137">출력</span><span class="sxs-lookup"><span data-stu-id="ec912-137">OUTPUTS</span></span>

## <span data-ttu-id="ec912-138">상속자</span><span class="sxs-lookup"><span data-stu-id="ec912-138">NOTES</span></span>

## <span data-ttu-id="ec912-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ec912-139">RELATED LINKS</span></span>

[<span data-ttu-id="ec912-140">Get-AzureVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="ec912-140">Get-AzureVMDscExtension</span></span>](./Get-AzureVMDscExtension.md)

[<span data-ttu-id="ec912-141">Set-AzureVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="ec912-141">Set-AzureVMDscExtension</span></span>](./Set-AzureVMDscExtension.md)

[<span data-ttu-id="ec912-142">업데이트-Add-azurevm</span><span class="sxs-lookup"><span data-stu-id="ec912-142">Update-AzureVM</span></span>](./Update-AzureVM.md)


