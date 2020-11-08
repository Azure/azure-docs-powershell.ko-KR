---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 268D3E91-AB0F-451F-93B2-9226985910B9
online version: ''
schema: 2.0.0
ms.openlocfilehash: 41648470b76d889c1ee9d47e4200f843e9f11522
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045849"
---
# <span data-ttu-id="4b903-101">Set-AzureVMPuppetExtension</span><span class="sxs-lookup"><span data-stu-id="4b903-101">Set-AzureVMPuppetExtension</span></span>

## <span data-ttu-id="4b903-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4b903-102">SYNOPSIS</span></span>
<span data-ttu-id="4b903-103">가상 컴퓨터에 대 한 퍼핏 확장을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4b903-103">Sets the Puppet extension for a virtual machine.</span></span>

## <span data-ttu-id="4b903-104">구문과</span><span class="sxs-lookup"><span data-stu-id="4b903-104">SYNTAX</span></span>

```
Set-AzureVMPuppetExtension [-PuppetMasterServer] <String> [[-Version] <String>] [-Disable]
 [[-ReferenceName] <String>] -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="4b903-105">설명은</span><span class="sxs-lookup"><span data-stu-id="4b903-105">DESCRIPTION</span></span>
<span data-ttu-id="4b903-106">**AzureVMPuppetExtension** cmdlet은 가상 컴퓨터에 대 한 퍼핏 확장을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4b903-106">The **Set-AzureVMPuppetExtension** cmdlet sets the Puppet extension for a virtual machine.</span></span>

## <span data-ttu-id="4b903-107">예제의</span><span class="sxs-lookup"><span data-stu-id="4b903-107">EXAMPLES</span></span>

### <span data-ttu-id="4b903-108">예제 1: 가상 컴퓨터에 대 한 퍼핏 확장 설정</span><span class="sxs-lookup"><span data-stu-id="4b903-108">Example 1: Set the Puppet extension for a virtual machine</span></span>
```
PS C:\> Set-AzureVMPuppetExtension -VM $VM
```

<span data-ttu-id="4b903-109">이 예제에서는 변수 $VM에 저장 되어 있는 지정 된 가상 컴퓨터에 대 한 퍼핏 확장을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4b903-109">This example sets the Puppet extension for the specified virtual machine as stored in the variable $VM.</span></span>

## <span data-ttu-id="4b903-110">변수</span><span class="sxs-lookup"><span data-stu-id="4b903-110">PARAMETERS</span></span>

### <span data-ttu-id="4b903-111">-Disable</span><span class="sxs-lookup"><span data-stu-id="4b903-111">-Disable</span></span>
<span data-ttu-id="4b903-112">이 cmdlet이 확장 상태를 사용 하지 않도록 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4b903-112">Indicates that this cmdlet disables the extension state.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4b903-113">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="4b903-113">-InformationAction</span></span>
<span data-ttu-id="4b903-114">이 cmdlet이 정보 이벤트에 응답 하는 방법을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4b903-114">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="4b903-115">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="4b903-115">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="4b903-116">하기로</span><span class="sxs-lookup"><span data-stu-id="4b903-116">Continue</span></span>
- <span data-ttu-id="4b903-117">숨기기</span><span class="sxs-lookup"><span data-stu-id="4b903-117">Ignore</span></span>
- <span data-ttu-id="4b903-118">Inquire</span><span class="sxs-lookup"><span data-stu-id="4b903-118">Inquire</span></span>
- <span data-ttu-id="4b903-119">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="4b903-119">SilentlyContinue</span></span>
- <span data-ttu-id="4b903-120">중지가</span><span class="sxs-lookup"><span data-stu-id="4b903-120">Stop</span></span>
- <span data-ttu-id="4b903-121">대기</span><span class="sxs-lookup"><span data-stu-id="4b903-121">Suspend</span></span>

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

### <span data-ttu-id="4b903-122">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="4b903-122">-InformationVariable</span></span>
<span data-ttu-id="4b903-123">정보 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4b903-123">Specifies an information variable.</span></span>

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

### <span data-ttu-id="4b903-124">-프로필</span><span class="sxs-lookup"><span data-stu-id="4b903-124">-Profile</span></span>
<span data-ttu-id="4b903-125">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4b903-125">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="4b903-126">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="4b903-126">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="4b903-127">-PuppetMasterServer</span><span class="sxs-lookup"><span data-stu-id="4b903-127">-PuppetMasterServer</span></span>
<span data-ttu-id="4b903-128">퍼핏 마스터 서버의 정규화 된 도메인 이름 (FQDN)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4b903-128">Specifies the fully qualified domain name (FQDN) of puppet master server.</span></span>

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

### <span data-ttu-id="4b903-129">-ReferenceName</span><span class="sxs-lookup"><span data-stu-id="4b903-129">-ReferenceName</span></span>
<span data-ttu-id="4b903-130">확장의 참조 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4b903-130">Specifies the reference name of the extension.</span></span>

<span data-ttu-id="4b903-131">확장을 참조 하는 데 사용 되는 사용자 정의 문자열입니다.</span><span class="sxs-lookup"><span data-stu-id="4b903-131">This is a user-defined string that is used to refer to an extension.</span></span>
<span data-ttu-id="4b903-132">이 파일은 확장이 가상 컴퓨터에 처음 추가 될 때 지정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4b903-132">It is specified when the extension is added to the virtual machine for the first time.</span></span>
<span data-ttu-id="4b903-133">후속 업데이트의 경우 확장을 업데이트할 때 이전에 사용한 참조 이름을 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="4b903-133">For subsequent updates, you need to specify the previously used reference name when you update the extension.</span></span>
<span data-ttu-id="4b903-134">확장명에 할당 된 ReferenceName은 **Get-add-azurevm** cmdlet을 사용 하 여 반환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4b903-134">The ReferenceName assigned to an extension is returned using the **Get-AzureVM** cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4b903-135">-버전</span><span class="sxs-lookup"><span data-stu-id="4b903-135">-Version</span></span>
<span data-ttu-id="4b903-136">확장 버전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4b903-136">Specifies the extension version.</span></span>

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

### <span data-ttu-id="4b903-137">-VM</span><span class="sxs-lookup"><span data-stu-id="4b903-137">-VM</span></span>
<span data-ttu-id="4b903-138">영구 가상 머신 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4b903-138">Specifies the persistent virtual machine object.</span></span>

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

### <span data-ttu-id="4b903-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b903-139">CommonParameters</span></span>
<span data-ttu-id="4b903-140">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="4b903-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4b903-141">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4b903-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b903-142">입력</span><span class="sxs-lookup"><span data-stu-id="4b903-142">INPUTS</span></span>

## <span data-ttu-id="4b903-143">출력</span><span class="sxs-lookup"><span data-stu-id="4b903-143">OUTPUTS</span></span>

## <span data-ttu-id="4b903-144">상속자</span><span class="sxs-lookup"><span data-stu-id="4b903-144">NOTES</span></span>

## <span data-ttu-id="4b903-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4b903-145">RELATED LINKS</span></span>

[<span data-ttu-id="4b903-146">다운로드-Add-azurevm</span><span class="sxs-lookup"><span data-stu-id="4b903-146">Get-AzureVM</span></span>](./Get-AzureVM.md)


