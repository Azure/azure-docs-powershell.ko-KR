---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: B98FCF46-A5D6-4CC9-B82A-60B429A21A8B
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8079844a931debee5b9338e98d405697cc4336f2
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045501"
---
# <span data-ttu-id="6adf9-101">Remove-AzureVMExtension</span><span class="sxs-lookup"><span data-stu-id="6adf9-101">Remove-AzureVMExtension</span></span>

## <span data-ttu-id="6adf9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6adf9-102">SYNOPSIS</span></span>
<span data-ttu-id="6adf9-103">가상 컴퓨터에서 리소스 확장을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="6adf9-103">Removes resource extensions from a virtual machine.</span></span>

## <span data-ttu-id="6adf9-104">구문과</span><span class="sxs-lookup"><span data-stu-id="6adf9-104">SYNTAX</span></span>

### <span data-ttu-id="6adf9-105">RemoveByExtensionName (기본값)</span><span class="sxs-lookup"><span data-stu-id="6adf9-105">RemoveByExtensionName (Default)</span></span>
```
Remove-AzureVMExtension [-ExtensionName] <String> [-Publisher] <String> -VM <IPersistentVM>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="6adf9-106">RemoveByReferenceName</span><span class="sxs-lookup"><span data-stu-id="6adf9-106">RemoveByReferenceName</span></span>
```
Remove-AzureVMExtension [-ReferenceName] <String> -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="6adf9-107">RemoveAll</span><span class="sxs-lookup"><span data-stu-id="6adf9-107">RemoveAll</span></span>
```
Remove-AzureVMExtension [-RemoveAll] -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="6adf9-108">설명은</span><span class="sxs-lookup"><span data-stu-id="6adf9-108">DESCRIPTION</span></span>
<span data-ttu-id="6adf9-109">**제거-AzureVMExtension** cmdlet은 가상 컴퓨터에서 리소스 확장을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="6adf9-109">The **Remove-AzureVMExtension** cmdlet removes resource extensions from a virtual machine.</span></span>

## <span data-ttu-id="6adf9-110">예제의</span><span class="sxs-lookup"><span data-stu-id="6adf9-110">EXAMPLES</span></span>

### <span data-ttu-id="6adf9-111">예제 1: 특정 이름 및 publisher를 사용 하 여 확장 제거</span><span class="sxs-lookup"><span data-stu-id="6adf9-111">Example 1: Remove an extension using a specific name and publisher</span></span>
```
PS C:\> $VM = Remove-AzureVMExtension -VM $VM -ExtensionName $EXT -Publisher $PUB;
```

<span data-ttu-id="6adf9-112">이 명령은 지정 된 이름 및 게시자의 확장명을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="6adf9-112">This command removes an extension with the specified name and publisher.</span></span>

### <span data-ttu-id="6adf9-113">예제 2: 특정 가상 컴퓨터에서 모든 확장 제거</span><span class="sxs-lookup"><span data-stu-id="6adf9-113">Example 2: Remove all extensions from a specific virtual machine</span></span>
```
PS C:\> $VM = Remove-AzureVMExtension -VM $VM -RemoveAll;
```

<span data-ttu-id="6adf9-114">이 명령은 $VM 변수에 저장 되어 있는 지정 된 가상 컴퓨터의 모든 확장을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="6adf9-114">This command removes all extensions from the specified virtual machine as stored in the variable $VM.</span></span>

## <span data-ttu-id="6adf9-115">변수</span><span class="sxs-lookup"><span data-stu-id="6adf9-115">PARAMETERS</span></span>

### <span data-ttu-id="6adf9-116">-ExtensionName</span><span class="sxs-lookup"><span data-stu-id="6adf9-116">-ExtensionName</span></span>
<span data-ttu-id="6adf9-117">이 cmdlet이 제거 하는 확장 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6adf9-117">Specifies the extension name that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: RemoveByExtensionName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6adf9-118">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="6adf9-118">-InformationAction</span></span>
<span data-ttu-id="6adf9-119">이 cmdlet이 정보 이벤트에 응답 하는 방법을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6adf9-119">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="6adf9-120">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="6adf9-120">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="6adf9-121">하기로</span><span class="sxs-lookup"><span data-stu-id="6adf9-121">Continue</span></span>
- <span data-ttu-id="6adf9-122">숨기기</span><span class="sxs-lookup"><span data-stu-id="6adf9-122">Ignore</span></span>
- <span data-ttu-id="6adf9-123">Inquire</span><span class="sxs-lookup"><span data-stu-id="6adf9-123">Inquire</span></span>
- <span data-ttu-id="6adf9-124">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="6adf9-124">SilentlyContinue</span></span>
- <span data-ttu-id="6adf9-125">중지가</span><span class="sxs-lookup"><span data-stu-id="6adf9-125">Stop</span></span>
- <span data-ttu-id="6adf9-126">대기</span><span class="sxs-lookup"><span data-stu-id="6adf9-126">Suspend</span></span>

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

### <span data-ttu-id="6adf9-127">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="6adf9-127">-InformationVariable</span></span>
<span data-ttu-id="6adf9-128">정보 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6adf9-128">Specifies an information variable.</span></span>

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

### <span data-ttu-id="6adf9-129">-프로필</span><span class="sxs-lookup"><span data-stu-id="6adf9-129">-Profile</span></span>
<span data-ttu-id="6adf9-130">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6adf9-130">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="6adf9-131">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="6adf9-131">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="6adf9-132">-Publisher</span><span class="sxs-lookup"><span data-stu-id="6adf9-132">-Publisher</span></span>
<span data-ttu-id="6adf9-133">확장 게시자를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6adf9-133">Specifies the extension publisher.</span></span>

```yaml
Type: String
Parameter Sets: RemoveByExtensionName
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6adf9-134">-ReferenceName</span><span class="sxs-lookup"><span data-stu-id="6adf9-134">-ReferenceName</span></span>
<span data-ttu-id="6adf9-135">확장의 참조 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6adf9-135">Specifies the reference name of the extension.</span></span>

```yaml
Type: String
Parameter Sets: RemoveByReferenceName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6adf9-136">-RemoveAll</span><span class="sxs-lookup"><span data-stu-id="6adf9-136">-RemoveAll</span></span>
<span data-ttu-id="6adf9-137">이 cmdlet이 가상 컴퓨터에서 모든 리소스 확장을 제거 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="6adf9-137">Indicates that this cmdlet removes all resource extensions from the virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: RemoveAll
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6adf9-138">-VM</span><span class="sxs-lookup"><span data-stu-id="6adf9-138">-VM</span></span>
<span data-ttu-id="6adf9-139">영구 가상 머신 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6adf9-139">Specifies the persistent virtual machine object.</span></span>

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

### <span data-ttu-id="6adf9-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6adf9-140">CommonParameters</span></span>
<span data-ttu-id="6adf9-141">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="6adf9-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6adf9-142">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6adf9-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6adf9-143">입력</span><span class="sxs-lookup"><span data-stu-id="6adf9-143">INPUTS</span></span>

## <span data-ttu-id="6adf9-144">출력</span><span class="sxs-lookup"><span data-stu-id="6adf9-144">OUTPUTS</span></span>

## <span data-ttu-id="6adf9-145">상속자</span><span class="sxs-lookup"><span data-stu-id="6adf9-145">NOTES</span></span>

## <span data-ttu-id="6adf9-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6adf9-146">RELATED LINKS</span></span>

[<span data-ttu-id="6adf9-147">Get-AzureVMExtension</span><span class="sxs-lookup"><span data-stu-id="6adf9-147">Get-AzureVMExtension</span></span>](./Get-AzureVMExtension.md)

[<span data-ttu-id="6adf9-148">Set-AzureVMExtension</span><span class="sxs-lookup"><span data-stu-id="6adf9-148">Set-AzureVMExtension</span></span>](./Set-AzureVMExtension.md)


