---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: D563ACF6-6BCD-4463-8731-175BA047A74D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2ceb2af6b359d5b9660397ef654d6c56e045ce64
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046166"
---
# <span data-ttu-id="75e44-101">Remove-AzureDataDisk</span><span class="sxs-lookup"><span data-stu-id="75e44-101">Remove-AzureDataDisk</span></span>

## <span data-ttu-id="75e44-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="75e44-102">SYNOPSIS</span></span>
<span data-ttu-id="75e44-103">Azure 가상 머신에서 데이터 디스크를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="75e44-103">Removes a data disk from an Azure virtual machine.</span></span>

## <span data-ttu-id="75e44-104">구문과</span><span class="sxs-lookup"><span data-stu-id="75e44-104">SYNTAX</span></span>

```
Remove-AzureDataDisk [-LUN] <Int32> [-DeleteVHD] -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="75e44-105">설명은</span><span class="sxs-lookup"><span data-stu-id="75e44-105">DESCRIPTION</span></span>
<span data-ttu-id="75e44-106">**제거-AzureDataDisk** Cmdlet은 Azure 가상 머신에서 데이터 디스크를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="75e44-106">The **Remove-AzureDataDisk** cmdlet removes a data disk from an Azure virtual machine.</span></span>
<span data-ttu-id="75e44-107">기본적으로이 cmdlet은 저장소 계정에서 데이터 디스크 blob을 제거 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="75e44-107">By default, this cmdlet does not remove the data disk blob from the storage account.</span></span>

## <span data-ttu-id="75e44-108">예제의</span><span class="sxs-lookup"><span data-stu-id="75e44-108">EXAMPLES</span></span>

### <span data-ttu-id="75e44-109">예제 1: 데이터 디스크 제거</span><span class="sxs-lookup"><span data-stu-id="75e44-109">Example 1: Remove a data disk</span></span>
```
PS C:\> Get-AzureVM -ServiceName "ContosoService" -Name "VirtualMachine07" | Remove-AzureDataDisk -LUN 0
```

<span data-ttu-id="75e44-110">이 명령은 VirtualMachine07 cmdlet을 사용 하 여 ContosoService 이라는 서비스의 가상 컴퓨터 (이름 = **)** 를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="75e44-110">This command gets the virtual machine named VirtualMachine07 in the service named ContosoService by using the **Get-AzureVM** cmdlet.</span></span>
<span data-ttu-id="75e44-111">이 명령은 파이프라인 연산자를 사용 하 여 가상 컴퓨터를 현재 cmdlet에 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="75e44-111">The command passes the virtual machine to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="75e44-112">현재 cmdlet은 LUN 0이 있는 데이터 디스크를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="75e44-112">The current cmdlet removes the data disk that has the LUN 0.</span></span>

### <span data-ttu-id="75e44-113">예제 2: 데이터 디스크 및 가상 하드 디스크 파일 제거</span><span class="sxs-lookup"><span data-stu-id="75e44-113">Example 2: Remove a data disk and the virtual hard disk file</span></span>
```
PS C:\> Get-AzureVM -ServiceName "ContosoService" -Name "VirtualMachine07" | Remove-AzureDataDisk -LUN 0 -DeleteVHD | Update-AzureVM
```

<span data-ttu-id="75e44-114">이 명령은 ContosoService 이라는 서비스에서 VirtualMachine07 이라는 가상 컴퓨터를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="75e44-114">This command gets the virtual machine named VirtualMachine07 in the service named ContosoService.</span></span>
<span data-ttu-id="75e44-115">명령이 가상 컴퓨터를 현재 cmdlet에 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="75e44-115">The command passes the virtual machine to the current cmdlet.</span></span>
<span data-ttu-id="75e44-116">현재 cmdlet은 LUN 0이 있는 데이터 디스크를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="75e44-116">The current cmdlet removes the data disk that has the LUN 0.</span></span>
<span data-ttu-id="75e44-117">명령에는 *Deletevhd* 매개 변수가 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="75e44-117">The command includes the *DeleteVHD* parameter.</span></span>
<span data-ttu-id="75e44-118">따라서 기본 가상 하드 디스크도 삭제 됩니다.</span><span class="sxs-lookup"><span data-stu-id="75e44-118">Therefore, it also deletes the underlying virtual hard disk.</span></span>
<span data-ttu-id="75e44-119">이 명령은 **업데이트-add-azurevm** cmdlet을 사용 하 여 변경 내용을 반영 하도록 가상 컴퓨터를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="75e44-119">The command updates the virtual machine to reflect your changes by using the **Update-AzureVM** cmdlet.</span></span>

## <span data-ttu-id="75e44-120">변수</span><span class="sxs-lookup"><span data-stu-id="75e44-120">PARAMETERS</span></span>

### <span data-ttu-id="75e44-121">-DeleteVHD</span><span class="sxs-lookup"><span data-stu-id="75e44-121">-DeleteVHD</span></span>
<span data-ttu-id="75e44-122">이 cmdlet이 blob 저장소에서 데이터 디스크와 VHD (가상 하드 디스크)를 제거 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="75e44-122">Indicates that this cmdlet removes the data disk and the virtual hard disk (VHD) from blob storage.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75e44-123">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="75e44-123">-InformationAction</span></span>
<span data-ttu-id="75e44-124">이 cmdlet이 정보 이벤트에 응답 하는 방법을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="75e44-124">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="75e44-125">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="75e44-125">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="75e44-126">하기로</span><span class="sxs-lookup"><span data-stu-id="75e44-126">Continue</span></span>
- <span data-ttu-id="75e44-127">숨기기</span><span class="sxs-lookup"><span data-stu-id="75e44-127">Ignore</span></span>
- <span data-ttu-id="75e44-128">Inquire</span><span class="sxs-lookup"><span data-stu-id="75e44-128">Inquire</span></span>
- <span data-ttu-id="75e44-129">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="75e44-129">SilentlyContinue</span></span>
- <span data-ttu-id="75e44-130">중지가</span><span class="sxs-lookup"><span data-stu-id="75e44-130">Stop</span></span>
- <span data-ttu-id="75e44-131">대기</span><span class="sxs-lookup"><span data-stu-id="75e44-131">Suspend</span></span>

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

### <span data-ttu-id="75e44-132">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="75e44-132">-InformationVariable</span></span>
<span data-ttu-id="75e44-133">정보 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="75e44-133">Specifies an information variable.</span></span>

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

### <span data-ttu-id="75e44-134">-LUN</span><span class="sxs-lookup"><span data-stu-id="75e44-134">-LUN</span></span>
<span data-ttu-id="75e44-135">가상 컴퓨터의 데이터 드라이브에 대 한 LUN (논리 단위 번호)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="75e44-135">Specifies the logical unit number (LUN) for the data drive in the virtual machine.</span></span>
<span data-ttu-id="75e44-136">유효한 값은 0 ~ 15입니다.</span><span class="sxs-lookup"><span data-stu-id="75e44-136">Valid values are: 0 through 15.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75e44-137">-프로필</span><span class="sxs-lookup"><span data-stu-id="75e44-137">-Profile</span></span>
<span data-ttu-id="75e44-138">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="75e44-138">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="75e44-139">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="75e44-139">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="75e44-140">-VM</span><span class="sxs-lookup"><span data-stu-id="75e44-140">-VM</span></span>
<span data-ttu-id="75e44-141">데이터 디스크에 연결 된 가상 컴퓨터 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="75e44-141">Specifies the virtual machine object that is attached to the data disk.</span></span>
<span data-ttu-id="75e44-142">가상 컴퓨터 개체를 가져오려면 **get-help** cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="75e44-142">To obtain a virtual machine object, use the **Get-AzureVM** cmdlet.</span></span>

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

### <span data-ttu-id="75e44-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75e44-143">CommonParameters</span></span>
<span data-ttu-id="75e44-144">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="75e44-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75e44-145">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="75e44-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75e44-146">입력</span><span class="sxs-lookup"><span data-stu-id="75e44-146">INPUTS</span></span>

## <span data-ttu-id="75e44-147">출력</span><span class="sxs-lookup"><span data-stu-id="75e44-147">OUTPUTS</span></span>

## <span data-ttu-id="75e44-148">상속자</span><span class="sxs-lookup"><span data-stu-id="75e44-148">NOTES</span></span>

## <span data-ttu-id="75e44-149">관련 링크</span><span class="sxs-lookup"><span data-stu-id="75e44-149">RELATED LINKS</span></span>

[<span data-ttu-id="75e44-150">-AzureDataDisk 추가</span><span class="sxs-lookup"><span data-stu-id="75e44-150">Add-AzureDataDisk</span></span>](./Add-AzureDataDisk.md)

[<span data-ttu-id="75e44-151">Get-AzureDataDisk</span><span class="sxs-lookup"><span data-stu-id="75e44-151">Get-AzureDataDisk</span></span>](./Get-AzureDataDisk.md)

[<span data-ttu-id="75e44-152">다운로드-Add-azurevm</span><span class="sxs-lookup"><span data-stu-id="75e44-152">Get-AzureVM</span></span>](./Get-AzureVM.md)

[<span data-ttu-id="75e44-153">Set AzureDataDisk</span><span class="sxs-lookup"><span data-stu-id="75e44-153">Set-AzureDataDisk</span></span>](./Set-AzureDataDisk.md)

[<span data-ttu-id="75e44-154">업데이트-Add-azurevm</span><span class="sxs-lookup"><span data-stu-id="75e44-154">Update-AzureVM</span></span>](./Update-AzureVM.md)


