---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 8F881112-3603-4EE7-88A4-ED45040A60AC
online version: ''
schema: 2.0.0
ms.openlocfilehash: ecc71708c0dff8e359813bb01db0f09f2c91a0cb
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045811"
---
# <span data-ttu-id="56534-101">Set-AzureVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="56534-101">Set-AzureVMAccessExtension</span></span>

## <span data-ttu-id="56534-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="56534-102">SYNOPSIS</span></span>
<span data-ttu-id="56534-103">가상 컴퓨터에 대 한 VMAccess 확장을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="56534-103">Sets the VMAccess extension for a virtual machine.</span></span>

## <span data-ttu-id="56534-104">구문과</span><span class="sxs-lookup"><span data-stu-id="56534-104">SYNTAX</span></span>

### <span data-ttu-id="56534-105">EnableAccessExtension (기본값)</span><span class="sxs-lookup"><span data-stu-id="56534-105">EnableAccessExtension (Default)</span></span>
```
Set-AzureVMAccessExtension [[-UserName] <String>] [[-Password] <String>] [[-ReferenceName] <String>]
 [[-Version] <String>] [-ForceUpdate] -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="56534-106">DisableAccessExtension</span><span class="sxs-lookup"><span data-stu-id="56534-106">DisableAccessExtension</span></span>
```
Set-AzureVMAccessExtension [-Disable] [[-ReferenceName] <String>] [[-Version] <String>] [-ForceUpdate]
 -VM <IPersistentVM> [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="56534-107">UninstallAccessExtension</span><span class="sxs-lookup"><span data-stu-id="56534-107">UninstallAccessExtension</span></span>
```
Set-AzureVMAccessExtension [-Uninstall] [[-ReferenceName] <String>] [[-Version] <String>] [-ForceUpdate]
 -VM <IPersistentVM> [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="56534-108">설명은</span><span class="sxs-lookup"><span data-stu-id="56534-108">DESCRIPTION</span></span>
<span data-ttu-id="56534-109">**AzureVMAccessExtension** cmdlet은 가상 컴퓨터에 가상 컴퓨터 Vmaccess 확장을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="56534-109">The **Set-AzureVMAccessExtension** cmdlet adds the Virtual Machine VMAccess Extension to a virtual machine.</span></span> <span data-ttu-id="56534-110">VMAccess 확장 프로그램은 임시 암호를 설정 하는 데 사용할 수 있으며, 컴퓨터에 로그인 한 후 즉시 변경 됩니다.</span><span class="sxs-lookup"><span data-stu-id="56534-110">VMAccess Extension can be used to set a temporary password and this should be immediately changed it after logging into the machine.</span></span>

## <span data-ttu-id="56534-111">예제의</span><span class="sxs-lookup"><span data-stu-id="56534-111">EXAMPLES</span></span>

### <span data-ttu-id="56534-112">예제 1: 지정 된 가상 컴퓨터에 적용 되는 VMAccess 확장 설정</span><span class="sxs-lookup"><span data-stu-id="56534-112">Example 1: Set the VMAccess extension applied to a specified virtual machine</span></span>
```
PS C:\> Set-AzureVMAccessExtension -VM $VM -UserName $User -Password $PWD;
```

<span data-ttu-id="56534-113">이 명령은 $VM 변수에 저장 되어 있는 지정 된 가상 컴퓨터에 적용 되는 VMAccess 확장을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="56534-113">This command sets the VMAccess extension applied to the specified virtual machine as stored in the variable $VM.</span></span>

## <span data-ttu-id="56534-114">변수</span><span class="sxs-lookup"><span data-stu-id="56534-114">PARAMETERS</span></span>

### <span data-ttu-id="56534-115">-Disable</span><span class="sxs-lookup"><span data-stu-id="56534-115">-Disable</span></span>
<span data-ttu-id="56534-116">이 cmdlet이 확장 상태를 사용 하지 않도록 설정 하는 것을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="56534-116">Indicates that this cmdlet sets the Extension State to Disable.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: DisableAccessExtension
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="56534-117">-ForceUpdate</span><span class="sxs-lookup"><span data-stu-id="56534-117">-ForceUpdate</span></span>
<span data-ttu-id="56534-118">이 cmdlet이 구성을 업데이트 하지 않은 경우 확장에 구성을 다시 적용 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="56534-118">Indicates that this cmdlet reapplies a configuration to an extension when the configuration has not been updated.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56534-119">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="56534-119">-InformationAction</span></span>
<span data-ttu-id="56534-120">이 cmdlet이 정보 이벤트에 응답 하는 방법을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="56534-120">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="56534-121">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="56534-121">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="56534-122">하기로</span><span class="sxs-lookup"><span data-stu-id="56534-122">Continue</span></span>
- <span data-ttu-id="56534-123">숨기기</span><span class="sxs-lookup"><span data-stu-id="56534-123">Ignore</span></span>
- <span data-ttu-id="56534-124">Inquire</span><span class="sxs-lookup"><span data-stu-id="56534-124">Inquire</span></span>
- <span data-ttu-id="56534-125">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="56534-125">SilentlyContinue</span></span>
- <span data-ttu-id="56534-126">중지가</span><span class="sxs-lookup"><span data-stu-id="56534-126">Stop</span></span>
- <span data-ttu-id="56534-127">대기</span><span class="sxs-lookup"><span data-stu-id="56534-127">Suspend</span></span>

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

### <span data-ttu-id="56534-128">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="56534-128">-InformationVariable</span></span>
<span data-ttu-id="56534-129">정보 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="56534-129">Specifies an information variable.</span></span>

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

### <span data-ttu-id="56534-130">-암호</span><span class="sxs-lookup"><span data-stu-id="56534-130">-Password</span></span>
<span data-ttu-id="56534-131">가상 컴퓨터의 자격 증명을 다시 설정 하기 위한 암호를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="56534-131">Specifies the password for resetting the virtual machine's credential.</span></span>

```yaml
Type: String
Parameter Sets: EnableAccessExtension
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="56534-132">-프로필</span><span class="sxs-lookup"><span data-stu-id="56534-132">-Profile</span></span>
<span data-ttu-id="56534-133">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="56534-133">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="56534-134">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="56534-134">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="56534-135">-ReferenceName</span><span class="sxs-lookup"><span data-stu-id="56534-135">-ReferenceName</span></span>
<span data-ttu-id="56534-136">Access 확장의 참조 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="56534-136">Specifies the reference name of the access extension.</span></span>

<span data-ttu-id="56534-137">확장을 참조 하는 데 사용 되는 사용자 정의 문자열입니다.</span><span class="sxs-lookup"><span data-stu-id="56534-137">This is a user-defined string that is used to refer to an extension.</span></span>
<span data-ttu-id="56534-138">이 파일은 확장이 가상 컴퓨터에 처음 추가 될 때 지정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="56534-138">It is specified when the extension is added to the virtual machine for the first time.</span></span>
<span data-ttu-id="56534-139">후속 업데이트의 경우 확장을 업데이트 하는 동안 이전에 사용한 참조 이름을 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="56534-139">For subsequent updates, you should specify the previously used reference name while updating the extension.</span></span>
<span data-ttu-id="56534-140">확장명에 할당 된 *Referencename* 은 **Get-add-azurevm** cmdlet을 사용 하 여 반환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="56534-140">The *ReferenceName* assigned to an extension is returned using the **Get-AzureVM** cmdlet.</span></span>

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

### <span data-ttu-id="56534-141">-제거</span><span class="sxs-lookup"><span data-stu-id="56534-141">-Uninstall</span></span>
<span data-ttu-id="56534-142">이 cmdlet이 access 확장을 제거 하는지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="56534-142">Indicates whether this cmdlet uninstalls the access extension.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: UninstallAccessExtension
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="56534-143">-사용자 이름</span><span class="sxs-lookup"><span data-stu-id="56534-143">-UserName</span></span>
<span data-ttu-id="56534-144">이 cmdlet이 가상 컴퓨터의 자격 증명을 다시 설정 하는 데 사용 하는 사용자 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="56534-144">Specifies the user name that this cmdlet uses to reset the virtual machine's credential.</span></span>

```yaml
Type: String
Parameter Sets: EnableAccessExtension
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="56534-145">-버전</span><span class="sxs-lookup"><span data-stu-id="56534-145">-Version</span></span>
<span data-ttu-id="56534-146">확장의 버전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="56534-146">Specifies the version of the extension.</span></span>

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

### <span data-ttu-id="56534-147">-VM</span><span class="sxs-lookup"><span data-stu-id="56534-147">-VM</span></span>
<span data-ttu-id="56534-148">영구 가상 머신 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="56534-148">Specifies the persistent virtual machine object.</span></span>

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

### <span data-ttu-id="56534-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56534-149">CommonParameters</span></span>
<span data-ttu-id="56534-150">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="56534-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56534-151">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="56534-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56534-152">입력</span><span class="sxs-lookup"><span data-stu-id="56534-152">INPUTS</span></span>

## <span data-ttu-id="56534-153">출력</span><span class="sxs-lookup"><span data-stu-id="56534-153">OUTPUTS</span></span>

## <span data-ttu-id="56534-154">상속자</span><span class="sxs-lookup"><span data-stu-id="56534-154">NOTES</span></span>

## <span data-ttu-id="56534-155">관련 링크</span><span class="sxs-lookup"><span data-stu-id="56534-155">RELATED LINKS</span></span>

[<span data-ttu-id="56534-156">Get-AzureVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="56534-156">Get-AzureVMAccessExtension</span></span>](./Get-AzureVMAccessExtension.md)

[<span data-ttu-id="56534-157">제거-AzureVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="56534-157">Remove-AzureVMAccessExtension</span></span>](./Remove-AzureVMAccessExtension.md)


