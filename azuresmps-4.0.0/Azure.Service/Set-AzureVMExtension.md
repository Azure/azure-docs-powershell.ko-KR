---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 97E9FB22-43A8-4D07-AF48-5884E4593CA9
online version: ''
schema: 2.0.0
ms.openlocfilehash: 35f3baea7440d58812056999ea4f271acf80b8d4
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045446"
---
# <span data-ttu-id="32acb-101">Set-AzureVMExtension</span><span class="sxs-lookup"><span data-stu-id="32acb-101">Set-AzureVMExtension</span></span>

## <span data-ttu-id="32acb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="32acb-102">SYNOPSIS</span></span>
<span data-ttu-id="32acb-103">가상 컴퓨터에 대 한 리소스 확장을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="32acb-103">Sets resource extensions for virtual machines.</span></span>

## <span data-ttu-id="32acb-104">구문과</span><span class="sxs-lookup"><span data-stu-id="32acb-104">SYNTAX</span></span>

### <span data-ttu-id="32acb-105">SetByExtensionName (기본값)</span><span class="sxs-lookup"><span data-stu-id="32acb-105">SetByExtensionName (Default)</span></span>
```
Set-AzureVMExtension [-ExtensionName] <String> [-Publisher] <String> [-Version] <String>
 [[-ReferenceName] <String>] [[-PublicConfiguration] <String>] [[-PrivateConfiguration] <String>] [-Disable]
 [-Uninstall] [[-PublicConfigKey] <String>] [[-PrivateConfigKey] <String>] [-ForceUpdate] -VM <IPersistentVM>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="32acb-106">SetByExtensionNameAndConfigFile</span><span class="sxs-lookup"><span data-stu-id="32acb-106">SetByExtensionNameAndConfigFile</span></span>
```
Set-AzureVMExtension [-ExtensionName] <String> [-Publisher] <String> [-Version] <String>
 [[-ReferenceName] <String>] [[-PublicConfigPath] <String>] [[-PrivateConfigPath] <String>] [-Disable]
 [-Uninstall] [[-PublicConfigKey] <String>] [[-PrivateConfigKey] <String>] [-ForceUpdate] -VM <IPersistentVM>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="32acb-107">SetByReferenceName</span><span class="sxs-lookup"><span data-stu-id="32acb-107">SetByReferenceName</span></span>
```
Set-AzureVMExtension [-ReferenceName] <String> [[-PublicConfiguration] <String>]
 [[-PrivateConfiguration] <String>] [-Disable] [-Uninstall] [[-PublicConfigKey] <String>]
 [[-PrivateConfigKey] <String>] [-ForceUpdate] -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="32acb-108">SetByReferenceNameAndConfigFile</span><span class="sxs-lookup"><span data-stu-id="32acb-108">SetByReferenceNameAndConfigFile</span></span>
```
Set-AzureVMExtension [-ReferenceName] <String> [[-PublicConfigPath] <String>] [[-PrivateConfigPath] <String>]
 [-Disable] [-Uninstall] [[-PublicConfigKey] <String>] [[-PrivateConfigKey] <String>] [-ForceUpdate]
 -VM <IPersistentVM> [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="32acb-109">설명은</span><span class="sxs-lookup"><span data-stu-id="32acb-109">DESCRIPTION</span></span>
<span data-ttu-id="32acb-110">**AzureVMExtension** cmdlet은 가상 컴퓨터에 대 한 리소스 확장을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="32acb-110">The **Set-AzureVMExtension** cmdlet sets resource extensions for virtual machines.</span></span>

## <span data-ttu-id="32acb-111">예제의</span><span class="sxs-lookup"><span data-stu-id="32acb-111">EXAMPLES</span></span>

### <span data-ttu-id="32acb-112">예제 1: 리소스 확장이 적용 된 가상 컴퓨터 만들기</span><span class="sxs-lookup"><span data-stu-id="32acb-112">Example 1: Create a virtual machine with resource extensions applied</span></span>
```
PS C:\> $X = New-AzureVMConfig -Name $VM -InstanceSize Small -ImageName $IMG;$X = Add-AzureProvisioningConfig -VM $X -Password $PWD -AdminUsername $USR -Windows;$X = Set-AzureVMExtension -VM $X -ExtensionName $Ext1 -Publisher $Publisher -Version $VER -PublicConfiguration $P1 -PrivateConfiguration $P2;$X = Set-AzureVMExtension -VM $X -ExtensionName $Ext2 -Publisher $Publisher -Version $VER -PublicConfiguration $P3 -PrivateConfiguration $P4;New-AzureVM -Location $LOC -ServiceName $SVC -VM $X;
```

<span data-ttu-id="32acb-113">이 명령은 리소스 확장이 적용 된 가상 컴퓨터를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="32acb-113">This command creates a virtual machine with resource extensions applied.</span></span>

## <span data-ttu-id="32acb-114">변수</span><span class="sxs-lookup"><span data-stu-id="32acb-114">PARAMETERS</span></span>

### <span data-ttu-id="32acb-115">-Disable</span><span class="sxs-lookup"><span data-stu-id="32acb-115">-Disable</span></span>
<span data-ttu-id="32acb-116">이 cmdlet이 확장 상태를 사용 하지 않도록 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="32acb-116">Indicates that this cmdlet disables the extension state.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="32acb-117">-ExtensionName</span><span class="sxs-lookup"><span data-stu-id="32acb-117">-ExtensionName</span></span>
<span data-ttu-id="32acb-118">가상 컴퓨터의 확장명 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="32acb-118">Specifies the extension name of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: SetByExtensionName, SetByExtensionNameAndConfigFile
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="32acb-119">-ForceUpdate</span><span class="sxs-lookup"><span data-stu-id="32acb-119">-ForceUpdate</span></span>
<span data-ttu-id="32acb-120">이 cmdlet이 구성을 업데이트 하지 않은 경우 확장에 구성을 다시 적용 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="32acb-120">Indicates that this cmdlet re-applies a configuration to an extension when the configuration has not been updated.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 11
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32acb-121">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="32acb-121">-InformationAction</span></span>
<span data-ttu-id="32acb-122">이 cmdlet이 정보 이벤트에 응답 하는 방법을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="32acb-122">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="32acb-123">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="32acb-123">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="32acb-124">하기로</span><span class="sxs-lookup"><span data-stu-id="32acb-124">Continue</span></span>
- <span data-ttu-id="32acb-125">숨기기</span><span class="sxs-lookup"><span data-stu-id="32acb-125">Ignore</span></span>
- <span data-ttu-id="32acb-126">Inquire</span><span class="sxs-lookup"><span data-stu-id="32acb-126">Inquire</span></span>
- <span data-ttu-id="32acb-127">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="32acb-127">SilentlyContinue</span></span>
- <span data-ttu-id="32acb-128">중지가</span><span class="sxs-lookup"><span data-stu-id="32acb-128">Stop</span></span>
- <span data-ttu-id="32acb-129">대기</span><span class="sxs-lookup"><span data-stu-id="32acb-129">Suspend</span></span>

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

### <span data-ttu-id="32acb-130">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="32acb-130">-InformationVariable</span></span>
<span data-ttu-id="32acb-131">정보 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="32acb-131">Specifies an information variable.</span></span>

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

### <span data-ttu-id="32acb-132">-PrivateConfigKey</span><span class="sxs-lookup"><span data-stu-id="32acb-132">-PrivateConfigKey</span></span>
<span data-ttu-id="32acb-133">개인 구성 키를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="32acb-133">Specifies a private configuration key.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="32acb-134">-PrivateConfigPath</span><span class="sxs-lookup"><span data-stu-id="32acb-134">-PrivateConfigPath</span></span>
<span data-ttu-id="32acb-135">개인 구성 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="32acb-135">Specifies the private configuration path.</span></span>

```yaml
Type: String
Parameter Sets: SetByExtensionNameAndConfigFile, SetByReferenceNameAndConfigFile
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="32acb-136">-PrivateConfiguration</span><span class="sxs-lookup"><span data-stu-id="32acb-136">-PrivateConfiguration</span></span>
<span data-ttu-id="32acb-137">개인 구성 텍스트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="32acb-137">Specifies the private configuration text.</span></span>

```yaml
Type: String
Parameter Sets: SetByExtensionName, SetByReferenceName
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="32acb-138">-프로필</span><span class="sxs-lookup"><span data-stu-id="32acb-138">-Profile</span></span>
<span data-ttu-id="32acb-139">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="32acb-139">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="32acb-140">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="32acb-140">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="32acb-141">-PublicConfigKey</span><span class="sxs-lookup"><span data-stu-id="32acb-141">-PublicConfigKey</span></span>
<span data-ttu-id="32acb-142">공개 구성 키를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="32acb-142">Specifies the public configuration key.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="32acb-143">-PublicConfigPath</span><span class="sxs-lookup"><span data-stu-id="32acb-143">-PublicConfigPath</span></span>
<span data-ttu-id="32acb-144">공용 구성 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="32acb-144">Specifies the public configuration path.</span></span>

```yaml
Type: String
Parameter Sets: SetByExtensionNameAndConfigFile, SetByReferenceNameAndConfigFile
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="32acb-145">-PublicConfiguration</span><span class="sxs-lookup"><span data-stu-id="32acb-145">-PublicConfiguration</span></span>
<span data-ttu-id="32acb-146">공용 구성 텍스트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="32acb-146">Specifies the public configuration text.</span></span>

```yaml
Type: String
Parameter Sets: SetByExtensionName, SetByReferenceName
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="32acb-147">-Publisher</span><span class="sxs-lookup"><span data-stu-id="32acb-147">-Publisher</span></span>
<span data-ttu-id="32acb-148">확장의 게시자를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="32acb-148">Specifies the publisher of the extension.</span></span>

```yaml
Type: String
Parameter Sets: SetByExtensionName, SetByExtensionNameAndConfigFile
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="32acb-149">-ReferenceName</span><span class="sxs-lookup"><span data-stu-id="32acb-149">-ReferenceName</span></span>
<span data-ttu-id="32acb-150">확장의 참조 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="32acb-150">Specifies the reference name of the extension.</span></span>

<span data-ttu-id="32acb-151">확장을 참조 하는 데 사용할 수 있는 사용자 정의 문자열입니다.</span><span class="sxs-lookup"><span data-stu-id="32acb-151">This is a user-defined string that can be used to refer to an extension.</span></span>
<span data-ttu-id="32acb-152">확장이 가상 컴퓨터에 처음 추가 될 때이를 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="32acb-152">You need to specify it when the extension is added to the virtual machine for the first time.</span></span>
<span data-ttu-id="32acb-153">후속 업데이트의 경우 확장을 업데이트 하는 동안 이전에 사용한 참조 이름을 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="32acb-153">For subsequent updates, you need to specify the previously used reference name while updating the extension.</span></span>
<span data-ttu-id="32acb-154">확장명에 할당 된 ReferenceName은 **Get-add-azurevm** cmdlet을 사용 하 여 반환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="32acb-154">The ReferenceName assigned to an extension is returned using the **Get-AzureVM** cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: SetByExtensionName, SetByExtensionNameAndConfigFile
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: SetByReferenceName, SetByReferenceNameAndConfigFile
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="32acb-155">-제거</span><span class="sxs-lookup"><span data-stu-id="32acb-155">-Uninstall</span></span>
<span data-ttu-id="32acb-156">이 cmdlet이 가상 컴퓨터에서 리소스 확장을 제거 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="32acb-156">Indicates that this cmdlet uninstalls the resource extension from the virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="32acb-157">-버전</span><span class="sxs-lookup"><span data-stu-id="32acb-157">-Version</span></span>
<span data-ttu-id="32acb-158">확장 버전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="32acb-158">Specifies the extension version.</span></span>

```yaml
Type: String
Parameter Sets: SetByExtensionName, SetByExtensionNameAndConfigFile
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="32acb-159">-VM</span><span class="sxs-lookup"><span data-stu-id="32acb-159">-VM</span></span>
<span data-ttu-id="32acb-160">영구 가상 머신 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="32acb-160">Specifies the persistent virtual machine object.</span></span>

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

### <span data-ttu-id="32acb-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="32acb-161">CommonParameters</span></span>
<span data-ttu-id="32acb-162">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="32acb-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="32acb-163">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="32acb-163">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="32acb-164">입력</span><span class="sxs-lookup"><span data-stu-id="32acb-164">INPUTS</span></span>

## <span data-ttu-id="32acb-165">출력</span><span class="sxs-lookup"><span data-stu-id="32acb-165">OUTPUTS</span></span>

## <span data-ttu-id="32acb-166">상속자</span><span class="sxs-lookup"><span data-stu-id="32acb-166">NOTES</span></span>

## <span data-ttu-id="32acb-167">관련 링크</span><span class="sxs-lookup"><span data-stu-id="32acb-167">RELATED LINKS</span></span>

[<span data-ttu-id="32acb-168">Get-AzureVMExtension</span><span class="sxs-lookup"><span data-stu-id="32acb-168">Get-AzureVMExtension</span></span>](./Get-AzureVMExtension.md)

[<span data-ttu-id="32acb-169">제거-AzureVMExtension</span><span class="sxs-lookup"><span data-stu-id="32acb-169">Remove-AzureVMExtension</span></span>](./Remove-AzureVMExtension.md)

[<span data-ttu-id="32acb-170">다운로드-Add-azurevm</span><span class="sxs-lookup"><span data-stu-id="32acb-170">Get-AzureVM</span></span>](./Get-AzureVM.md)


