---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 377716B6-8B8C-4CAE-A8FA-835DA24F04C7
online version: ''
schema: 2.0.0
ms.openlocfilehash: c9610c6b8abaf4d59d6a363253d0b90a0dfcecad
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046043"
---
# <span data-ttu-id="f237f-101">Set-AzureVMBGInfoExtension</span><span class="sxs-lookup"><span data-stu-id="f237f-101">Set-AzureVMBGInfoExtension</span></span>

## <span data-ttu-id="f237f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f237f-102">SYNOPSIS</span></span>
<span data-ttu-id="f237f-103">가상 컴퓨터에 대 한 BGInfo 확장을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f237f-103">Sets the BGInfo extension for a virtual machine.</span></span>

## <span data-ttu-id="f237f-104">구문과</span><span class="sxs-lookup"><span data-stu-id="f237f-104">SYNTAX</span></span>

### <span data-ttu-id="f237f-105">SetBGInfoExtension (기본값)</span><span class="sxs-lookup"><span data-stu-id="f237f-105">SetBGInfoExtension (Default)</span></span>
```
Set-AzureVMBGInfoExtension [-Disable] [[-ReferenceName] <String>] [[-Version] <String>] -VM <IPersistentVM>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="f237f-106">UninstallBGInfoExtension</span><span class="sxs-lookup"><span data-stu-id="f237f-106">UninstallBGInfoExtension</span></span>
```
Set-AzureVMBGInfoExtension [-Uninstall] [[-ReferenceName] <String>] [[-Version] <String>] -VM <IPersistentVM>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="f237f-107">설명은</span><span class="sxs-lookup"><span data-stu-id="f237f-107">DESCRIPTION</span></span>
<span data-ttu-id="f237f-108">**AzureVMBGInfoExtension** cmdlet은 가상 컴퓨터에 대 한 BGInfo 확장을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f237f-108">The **Set-AzureVMBGInfoExtension** cmdlet sets the BGInfo extension for a virtual machine.</span></span>

## <span data-ttu-id="f237f-109">예제의</span><span class="sxs-lookup"><span data-stu-id="f237f-109">EXAMPLES</span></span>

### <span data-ttu-id="f237f-110">예제 1: 가상 컴퓨터에 대 한 BGInfo 확장 설정</span><span class="sxs-lookup"><span data-stu-id="f237f-110">Example 1: Set the BGInfo extension for a virtual machine</span></span>
```
PS C:\> Set-AzureVMBGInfoExtension -VM $VM
```

<span data-ttu-id="f237f-111">이 명령은 $VM 변수에 저장 되는 지정 된 가상 컴퓨터의 BGInfo 확장명을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f237f-111">This command sets the BGInfo extension for the specified virtual machine as stored in the variable $VM.</span></span>

## <span data-ttu-id="f237f-112">변수</span><span class="sxs-lookup"><span data-stu-id="f237f-112">PARAMETERS</span></span>

### <span data-ttu-id="f237f-113">-Disable</span><span class="sxs-lookup"><span data-stu-id="f237f-113">-Disable</span></span>
<span data-ttu-id="f237f-114">이 cmdlet이 확장 상태를 사용 하지 않도록 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f237f-114">Indicates that this cmdlet disables the extension state.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: SetBGInfoExtension
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f237f-115">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="f237f-115">-InformationAction</span></span>
<span data-ttu-id="f237f-116">이 cmdlet이 정보 이벤트에 응답 하는 방법을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f237f-116">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="f237f-117">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="f237f-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="f237f-118">하기로</span><span class="sxs-lookup"><span data-stu-id="f237f-118">Continue</span></span>
- <span data-ttu-id="f237f-119">숨기기</span><span class="sxs-lookup"><span data-stu-id="f237f-119">Ignore</span></span>
- <span data-ttu-id="f237f-120">Inquire</span><span class="sxs-lookup"><span data-stu-id="f237f-120">Inquire</span></span>
- <span data-ttu-id="f237f-121">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="f237f-121">SilentlyContinue</span></span>
- <span data-ttu-id="f237f-122">중지가</span><span class="sxs-lookup"><span data-stu-id="f237f-122">Stop</span></span>
- <span data-ttu-id="f237f-123">대기</span><span class="sxs-lookup"><span data-stu-id="f237f-123">Suspend</span></span>

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

### <span data-ttu-id="f237f-124">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="f237f-124">-InformationVariable</span></span>
<span data-ttu-id="f237f-125">정보 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f237f-125">Specifies an information variable.</span></span>

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

### <span data-ttu-id="f237f-126">-프로필</span><span class="sxs-lookup"><span data-stu-id="f237f-126">-Profile</span></span>
<span data-ttu-id="f237f-127">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f237f-127">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="f237f-128">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="f237f-128">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="f237f-129">-ReferenceName</span><span class="sxs-lookup"><span data-stu-id="f237f-129">-ReferenceName</span></span>
<span data-ttu-id="f237f-130">BGInfo 확장의 참조 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f237f-130">Specifies the reference name of the BGInfo extension.</span></span>

<span data-ttu-id="f237f-131">이 매개 변수는 확장을 참조 하는 데 사용할 수 있는 사용자 정의 문자열입니다.</span><span class="sxs-lookup"><span data-stu-id="f237f-131">This parameter is a user-defined string that can be used to refer to an extension.</span></span>
<span data-ttu-id="f237f-132">이 파일은 확장이 가상 컴퓨터에 처음 추가 될 때 지정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="f237f-132">It is specified when the extension is added to the virtual machine for the first time.</span></span>
<span data-ttu-id="f237f-133">확장을 업데이트 하는 동안 이전에 사용한 참조 이름을 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f237f-133">You can specify the previously used reference name while updating the extension.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f237f-134">-제거</span><span class="sxs-lookup"><span data-stu-id="f237f-134">-Uninstall</span></span>
<span data-ttu-id="f237f-135">이 cmdlet이 BGInfo 확장을 제거 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="f237f-135">Indicates that this cmdlet uninstalls the BGInfo extension.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: UninstallBGInfoExtension
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f237f-136">-버전</span><span class="sxs-lookup"><span data-stu-id="f237f-136">-Version</span></span>
<span data-ttu-id="f237f-137">BGInfo 확장명의 버전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f237f-137">Specifies the version of the BGInfo extension.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f237f-138">-VM</span><span class="sxs-lookup"><span data-stu-id="f237f-138">-VM</span></span>
<span data-ttu-id="f237f-139">영구 가상 머신 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f237f-139">Specifies the persistent virtual machine object.</span></span>

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

### <span data-ttu-id="f237f-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f237f-140">CommonParameters</span></span>
<span data-ttu-id="f237f-141">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f237f-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f237f-142">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f237f-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f237f-143">입력</span><span class="sxs-lookup"><span data-stu-id="f237f-143">INPUTS</span></span>

## <span data-ttu-id="f237f-144">출력</span><span class="sxs-lookup"><span data-stu-id="f237f-144">OUTPUTS</span></span>

## <span data-ttu-id="f237f-145">상속자</span><span class="sxs-lookup"><span data-stu-id="f237f-145">NOTES</span></span>

## <span data-ttu-id="f237f-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f237f-146">RELATED LINKS</span></span>

[<span data-ttu-id="f237f-147">Get-AzureVMBGInfoExtension</span><span class="sxs-lookup"><span data-stu-id="f237f-147">Get-AzureVMBGInfoExtension</span></span>](./Get-AzureVMBGInfoExtension.md)

[<span data-ttu-id="f237f-148">제거-AzureVMBGInfoExtension</span><span class="sxs-lookup"><span data-stu-id="f237f-148">Remove-AzureVMBGInfoExtension</span></span>](./Remove-AzureVMBGInfoExtension.md)


