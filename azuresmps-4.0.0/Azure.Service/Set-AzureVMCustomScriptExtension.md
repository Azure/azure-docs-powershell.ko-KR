---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 6A8F07D1-AC20-4950-9019-BDFB4FD3CF69
online version: ''
schema: 2.0.0
ms.openlocfilehash: a7569e203369bf1177b4eecc2bd689f3e20dcd48
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046037"
---
# <span data-ttu-id="b4639-101">Set-AzureVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="b4639-101">Set-AzureVMCustomScriptExtension</span></span>

## <span data-ttu-id="b4639-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b4639-102">SYNOPSIS</span></span>
<span data-ttu-id="b4639-103">Azure virtual machine 사용자 지정 스크립트 확장에 대 한 정보를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b4639-103">Sets information for an Azure virtual machine custom script extension.</span></span>

## <span data-ttu-id="b4639-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b4639-104">SYNTAX</span></span>

### <span data-ttu-id="b4639-105">SetCustomScriptExtensionByContainerAndFileNames (기본값)</span><span class="sxs-lookup"><span data-stu-id="b4639-105">SetCustomScriptExtensionByContainerAndFileNames (Default)</span></span>
```
Set-AzureVMCustomScriptExtension [[-ReferenceName] <String>] [[-Version] <String>] [-ContainerName] <String>
 [-FileName] <String[]> [[-StorageAccountName] <String>] [[-StorageEndpointSuffix] <String>]
 [[-StorageAccountKey] <String>] [[-Run] <String>] [[-Argument] <String>] [-ForceUpdate] -VM <IPersistentVM>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="b4639-106">DisableCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="b4639-106">DisableCustomScriptExtension</span></span>
```
Set-AzureVMCustomScriptExtension [[-ReferenceName] <String>] [[-Version] <String>] [-Disable] [-ForceUpdate]
 -VM <IPersistentVM> [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="b4639-107">UninstalleCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="b4639-107">UninstalleCustomScriptExtension</span></span>
```
Set-AzureVMCustomScriptExtension [[-ReferenceName] <String>] [[-Version] <String>] [-Uninstall] [-ForceUpdate]
 -VM <IPersistentVM> [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="b4639-108">SetCustomScriptExtensionByUriLinks</span><span class="sxs-lookup"><span data-stu-id="b4639-108">SetCustomScriptExtensionByUriLinks</span></span>
```
Set-AzureVMCustomScriptExtension [[-ReferenceName] <String>] [[-Version] <String>] [[-FileUri] <String[]>]
 [-Run] <String> [[-Argument] <String>] [-ForceUpdate] -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="b4639-109">설명은</span><span class="sxs-lookup"><span data-stu-id="b4639-109">DESCRIPTION</span></span>
<span data-ttu-id="b4639-110">**AzureVMCustomScriptExtension** Cmdlet은 Azure virtual machine 사용자 지정 스크립트 확장에 대 한 정보를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b4639-110">The **Set-AzureVMCustomScriptExtension** cmdlet sets information for an Azure virtual machine custom script extension.</span></span>

## <span data-ttu-id="b4639-111">예제의</span><span class="sxs-lookup"><span data-stu-id="b4639-111">EXAMPLES</span></span>

### <span data-ttu-id="b4639-112">예제 1: 가상 컴퓨터 사용자 지정 스크립트 확장에 대 한 정보 설정</span><span class="sxs-lookup"><span data-stu-id="b4639-112">Example 1: Set information for a virtual machine custom script extension</span></span>
```
PS C:\> $VM = Set-AzureVMCustomScriptExtension -VM $VM -ContainerName "Container01" -FileName "script1.ps1","script2.ps1" -Run "script1.ps1" -Argument "arg1 arg2";
PS C:\> New-AzureVM -Location "West US" -ServiceName $SVC -VM $VM;
```

<span data-ttu-id="b4639-113">이 명령은 가상 컴퓨터 사용자 지정 스크립트 확장에 대 한 정보를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b4639-113">This command sets information for a virtual machine custom script extension.</span></span>

### <span data-ttu-id="b4639-114">예제 2: 파일 경로를 사용 하 여 가상 컴퓨터 사용자 지정 스크립트 확장명에 대 한 정보 설정</span><span class="sxs-lookup"><span data-stu-id="b4639-114">Example 2: Set information for a virtual machine custom script extension using a file path</span></span>
```
PS C:\> Set-AzureVMCustomScriptExtension -VM $VM -FileUri "http://www.blob.core.contoso.net/bar/script1.ps1","http://www.blob.core.contoso.net/baz/script2.ps1" -Run "script1.ps1" -Argument "arg1 arg2";
PS C:\> Update-AzureVM -ServiceName $SVC -Name $Name -VM VM;
```

<span data-ttu-id="b4639-115">이 명령은 여러 파일 Url을 사용 하 여 가상 머신 사용자 지정 스크립트 확장에 대 한 정보를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b4639-115">This command sets information for a virtual machine custom script extension using multiple file URLs.</span></span>

## <span data-ttu-id="b4639-116">변수</span><span class="sxs-lookup"><span data-stu-id="b4639-116">PARAMETERS</span></span>

### <span data-ttu-id="b4639-117">-인수</span><span class="sxs-lookup"><span data-stu-id="b4639-117">-Argument</span></span>
<span data-ttu-id="b4639-118">이 cmdlet이 가상 컴퓨터에서 실행 하는 인수를 제공 하는 문자열을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b4639-118">Specifies a string that supplies an argument that this cmdlet runs on the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: SetCustomScriptExtensionByContainerAndFileNames, SetCustomScriptExtensionByUriLinks
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b4639-119">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="b4639-119">-ContainerName</span></span>
<span data-ttu-id="b4639-120">저장소 계정 내에서 컨테이너 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b4639-120">Specifies the container name within the storage account.</span></span>

```yaml
Type: String
Parameter Sets: SetCustomScriptExtensionByContainerAndFileNames
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b4639-121">-Disable</span><span class="sxs-lookup"><span data-stu-id="b4639-121">-Disable</span></span>
<span data-ttu-id="b4639-122">이 cmdlet이 확장 상태를 사용 하지 않도록 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b4639-122">Indicates that this cmdlet disables the extension state.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: DisableCustomScriptExtension
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b4639-123">-FileName</span><span class="sxs-lookup"><span data-stu-id="b4639-123">-FileName</span></span>
<span data-ttu-id="b4639-124">지정 된 컨테이너에 있는 blob 파일의 이름을 포함 하는 문자열 배열을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b4639-124">Specifies a string array that contains the names of the blob files in the specified container.</span></span>

```yaml
Type: String[]
Parameter Sets: SetCustomScriptExtensionByContainerAndFileNames
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b4639-125">-FileUri</span><span class="sxs-lookup"><span data-stu-id="b4639-125">-FileUri</span></span>
<span data-ttu-id="b4639-126">Blob 파일의 Url을 포함 하는 문자열 배열을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b4639-126">Specifies a string array that contains the URLs of the blob files.</span></span>

```yaml
Type: String[]
Parameter Sets: SetCustomScriptExtensionByUriLinks
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b4639-127">-ForceUpdate</span><span class="sxs-lookup"><span data-stu-id="b4639-127">-ForceUpdate</span></span>
<span data-ttu-id="b4639-128">이 cmdlet이 구성을 업데이트 하지 않은 경우 확장에 구성을 다시 적용 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="b4639-128">Indicates that this cmdlet re-apply a configuration to an extension when the configuration has not been updated.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 9
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4639-129">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="b4639-129">-InformationAction</span></span>
<span data-ttu-id="b4639-130">이 cmdlet이 정보 이벤트에 응답 하는 방법을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b4639-130">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="b4639-131">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="b4639-131">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="b4639-132">하기로</span><span class="sxs-lookup"><span data-stu-id="b4639-132">Continue</span></span>
- <span data-ttu-id="b4639-133">숨기기</span><span class="sxs-lookup"><span data-stu-id="b4639-133">Ignore</span></span>
- <span data-ttu-id="b4639-134">Inquire</span><span class="sxs-lookup"><span data-stu-id="b4639-134">Inquire</span></span>
- <span data-ttu-id="b4639-135">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="b4639-135">SilentlyContinue</span></span>
- <span data-ttu-id="b4639-136">중지가</span><span class="sxs-lookup"><span data-stu-id="b4639-136">Stop</span></span>
- <span data-ttu-id="b4639-137">대기</span><span class="sxs-lookup"><span data-stu-id="b4639-137">Suspend</span></span>

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

### <span data-ttu-id="b4639-138">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="b4639-138">-InformationVariable</span></span>
<span data-ttu-id="b4639-139">정보 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b4639-139">Specifies an information variable.</span></span>

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

### <span data-ttu-id="b4639-140">-프로필</span><span class="sxs-lookup"><span data-stu-id="b4639-140">-Profile</span></span>
<span data-ttu-id="b4639-141">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b4639-141">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="b4639-142">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="b4639-142">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="b4639-143">-ReferenceName</span><span class="sxs-lookup"><span data-stu-id="b4639-143">-ReferenceName</span></span>
<span data-ttu-id="b4639-144">확장명에 대 한 참조 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b4639-144">Specifies the reference name for the extension.</span></span>

<span data-ttu-id="b4639-145">이 매개 변수는 확장을 참조 하는 데 사용할 수 있는 사용자 정의 문자열입니다.</span><span class="sxs-lookup"><span data-stu-id="b4639-145">This parameter is a user-defined string that can be used to refer to an extension.</span></span>
<span data-ttu-id="b4639-146">이 파일은 확장이 가상 컴퓨터에 처음 추가 될 때 지정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b4639-146">It is specified when the extension is added to the virtual machine for the first time.</span></span>
<span data-ttu-id="b4639-147">후속 업데이트의 경우 확장을 업데이트 하는 동안 이전에 사용한 참조 이름을 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b4639-147">For subsequent updates, you need to specify the previously used reference name while updating the extension.</span></span>
<span data-ttu-id="b4639-148">확장명에 할당 된 *Referencename* 은 **Get-add-azurevm** cmdlet을 사용 하 여 반환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b4639-148">The *ReferenceName* assigned to an extension is returned using the **Get-AzureVM** cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b4639-149">-실행</span><span class="sxs-lookup"><span data-stu-id="b4639-149">-Run</span></span>
<span data-ttu-id="b4639-150">이 cmdlet이 가상 컴퓨터의 확장에 의해 실행 되는 명령을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b4639-150">Specifies the command this cmdlet runs by the extension on the virtual machine.</span></span>
<span data-ttu-id="b4639-151">"powershell.exe"만 지원 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b4639-151">Only "powershell.exe" is supported.</span></span>

```yaml
Type: String
Parameter Sets: SetCustomScriptExtensionByContainerAndFileNames
Aliases: RunFile, Command

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: SetCustomScriptExtensionByUriLinks
Aliases: RunFile, Command

Required: True
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b4639-152">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="b4639-152">-StorageAccountKey</span></span>
<span data-ttu-id="b4639-153">저장소 계정 키를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b4639-153">Specifies the storage account key</span></span>

```yaml
Type: String
Parameter Sets: SetCustomScriptExtensionByContainerAndFileNames
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b4639-154">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="b4639-154">-StorageAccountName</span></span>
<span data-ttu-id="b4639-155">현재 구독에서 저장소 계정 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b4639-155">Specifies the storage account name in the current subscription.</span></span>

```yaml
Type: String
Parameter Sets: SetCustomScriptExtensionByContainerAndFileNames
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b4639-156">-StorageEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="b4639-156">-StorageEndpointSuffix</span></span>
<span data-ttu-id="b4639-157">저장소 서비스 끝점을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b4639-157">Specifies the storage service endpoint.</span></span>

```yaml
Type: String
Parameter Sets: SetCustomScriptExtensionByContainerAndFileNames
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b4639-158">-제거</span><span class="sxs-lookup"><span data-stu-id="b4639-158">-Uninstall</span></span>
<span data-ttu-id="b4639-159">이 cmdlet이 가상 머신에서 사용자 지정 스크립트 확장을 제거 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="b4639-159">Indicates that this cmdlet uninstalls the custom script extension from the virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: UninstalleCustomScriptExtension
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b4639-160">-버전</span><span class="sxs-lookup"><span data-stu-id="b4639-160">-Version</span></span>
<span data-ttu-id="b4639-161">사용자 지정 스크립트 확장 버전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b4639-161">Specifies the version of the custom script extension.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b4639-162">-VM</span><span class="sxs-lookup"><span data-stu-id="b4639-162">-VM</span></span>
<span data-ttu-id="b4639-163">영구 가상 머신 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b4639-163">Specifies the persistent virtual machine object.</span></span>

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

### <span data-ttu-id="b4639-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4639-164">CommonParameters</span></span>
<span data-ttu-id="b4639-165">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b4639-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4639-166">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b4639-166">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4639-167">입력</span><span class="sxs-lookup"><span data-stu-id="b4639-167">INPUTS</span></span>

## <span data-ttu-id="b4639-168">출력</span><span class="sxs-lookup"><span data-stu-id="b4639-168">OUTPUTS</span></span>

## <span data-ttu-id="b4639-169">상속자</span><span class="sxs-lookup"><span data-stu-id="b4639-169">NOTES</span></span>

## <span data-ttu-id="b4639-170">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b4639-170">RELATED LINKS</span></span>

[<span data-ttu-id="b4639-171">Get-AzureVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="b4639-171">Get-AzureVMCustomScriptExtension</span></span>](./Get-AzureVMCustomScriptExtension.md)

[<span data-ttu-id="b4639-172">제거-AzureVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="b4639-172">Remove-AzureVMCustomScriptExtension</span></span>](./Remove-AzureVMCustomScriptExtension.md)

[<span data-ttu-id="b4639-173">다운로드-Add-azurevm</span><span class="sxs-lookup"><span data-stu-id="b4639-173">Get-AzureVM</span></span>](./Get-AzureVM.md)


