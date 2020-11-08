---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 8DC10708-09CE-449C-BE20-1E9E49CCE08A
online version: ''
schema: 2.0.0
ms.openlocfilehash: 55d9879d6e6768bf3ad409c84a4fc1052d58d8b3
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046013"
---
# <span data-ttu-id="23f98-101">Update-AzureVM</span><span class="sxs-lookup"><span data-stu-id="23f98-101">Update-AzureVM</span></span>

## <span data-ttu-id="23f98-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="23f98-102">SYNOPSIS</span></span>
<span data-ttu-id="23f98-103">Azure 가상 컴퓨터의 구성을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="23f98-103">Modifies the configuration of an Azure virtual machine.</span></span>

## <span data-ttu-id="23f98-104">구문과</span><span class="sxs-lookup"><span data-stu-id="23f98-104">SYNTAX</span></span>

```
Update-AzureVM [-Name] <String> -VM <PersistentVM> [-ServiceName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="23f98-105">설명은</span><span class="sxs-lookup"><span data-stu-id="23f98-105">DESCRIPTION</span></span>
<span data-ttu-id="23f98-106">**업데이트-add-azurevm** cmdlet은 지정 된 가상 컴퓨터에 대 한 업데이트 정보를 수락 하 고 업데이트를 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="23f98-106">The **Update-AzureVM** cmdlet accepts update information for the specified virtual machine and initiates the update.</span></span>
<span data-ttu-id="23f98-107">데이터 디스크를 추가 또는 제거 하거나, 데이터 또는 운영 체제 디스크의 캐시 모드를 수정 하거나, 네트워크 끝점을 변경 하거나, 가상 컴퓨터 크기를 변경할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="23f98-107">You can add or remove data disks, modify the cache mode of data or operating system disks, change the network endpoints, or change the size of the virtual machine.</span></span>

## <span data-ttu-id="23f98-108">예제의</span><span class="sxs-lookup"><span data-stu-id="23f98-108">EXAMPLES</span></span>

### <span data-ttu-id="23f98-109">예제 1: 가상 컴퓨터의 크기 업데이트</span><span class="sxs-lookup"><span data-stu-id="23f98-109">Example 1: Update the size of a virtual machine</span></span>
```
PS C:\> Get-AzureVM -ServiceName "ContosoService03" -Name "VirtualMachine04" | Set-AzureVMSize -InstanceSize "Medium" | Update-AzureVM
```

<span data-ttu-id="23f98-110">이 명령은 ContosoService03 라는 서비스에서 실행 되는 VirtualMachine04 이라는 가상 컴퓨터의 크기를 중간으로 변경 합니다.</span><span class="sxs-lookup"><span data-stu-id="23f98-110">This command changes the size of the virtual machine named VirtualMachine04, running in the service named ContosoService03, to Medium.</span></span>

### <span data-ttu-id="23f98-111">예제 2: 가상 컴퓨터에 데이터 디스크 추가</span><span class="sxs-lookup"><span data-stu-id="23f98-111">Example 2: Add a data disk to a virtual machine</span></span>
```
PS C:\> Get-AzureVM -ServiceName "ContosoService03" -Name "VirtualMachine05" | Add-AzureDataDisk -CreateNew -MediaLocation "https://ContosoStore1.blob.core.azure.com/vhds/Disk22.vhd" -DiskSizeInGB 128 -DiskLabel "Data-128" -LUN 0 | Update-AzureVM
```

<span data-ttu-id="23f98-112">이 명령은 ContosoService03 이라는 서비스에서 실행 되는 VirtualMachine05 이라는 가상 컴퓨터에 새 데이터 디스크를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="23f98-112">This command adds a new data disk to the virtual machine named VirtualMachine05, running in the service named ContosoService03.</span></span>

## <span data-ttu-id="23f98-113">변수</span><span class="sxs-lookup"><span data-stu-id="23f98-113">PARAMETERS</span></span>

### <span data-ttu-id="23f98-114">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="23f98-114">-InformationAction</span></span>
<span data-ttu-id="23f98-115">이 cmdlet이 정보 이벤트에 응답 하는 방법을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="23f98-115">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="23f98-116">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="23f98-116">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="23f98-117">하기로</span><span class="sxs-lookup"><span data-stu-id="23f98-117">Continue</span></span>
- <span data-ttu-id="23f98-118">숨기기</span><span class="sxs-lookup"><span data-stu-id="23f98-118">Ignore</span></span>
- <span data-ttu-id="23f98-119">Inquire</span><span class="sxs-lookup"><span data-stu-id="23f98-119">Inquire</span></span>
- <span data-ttu-id="23f98-120">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="23f98-120">SilentlyContinue</span></span>
- <span data-ttu-id="23f98-121">중지가</span><span class="sxs-lookup"><span data-stu-id="23f98-121">Stop</span></span>
- <span data-ttu-id="23f98-122">대기</span><span class="sxs-lookup"><span data-stu-id="23f98-122">Suspend</span></span>

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

### <span data-ttu-id="23f98-123">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="23f98-123">-InformationVariable</span></span>
<span data-ttu-id="23f98-124">정보 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="23f98-124">Specifies an information variable.</span></span>

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

### <span data-ttu-id="23f98-125">-이름</span><span class="sxs-lookup"><span data-stu-id="23f98-125">-Name</span></span>
<span data-ttu-id="23f98-126">업데이트할 가상 컴퓨터의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="23f98-126">Specifies the name of the virtual machine to update.</span></span>

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

### <span data-ttu-id="23f98-127">-프로필</span><span class="sxs-lookup"><span data-stu-id="23f98-127">-Profile</span></span>
<span data-ttu-id="23f98-128">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="23f98-128">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="23f98-129">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="23f98-129">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="23f98-130">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="23f98-130">-ServiceName</span></span>
<span data-ttu-id="23f98-131">Azure 서비스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="23f98-131">Specifies the name of the Azure service.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="23f98-132">-VM</span><span class="sxs-lookup"><span data-stu-id="23f98-132">-VM</span></span>
<span data-ttu-id="23f98-133">업데이트 된 설정을 포함 하는 가상 컴퓨터 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="23f98-133">Specifies the virtual machine object that includes updated settings.</span></span>

```yaml
Type: PersistentVM
Parameter Sets: (All)
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="23f98-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23f98-134">CommonParameters</span></span>
<span data-ttu-id="23f98-135">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="23f98-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23f98-136">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="23f98-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23f98-137">입력</span><span class="sxs-lookup"><span data-stu-id="23f98-137">INPUTS</span></span>

## <span data-ttu-id="23f98-138">출력</span><span class="sxs-lookup"><span data-stu-id="23f98-138">OUTPUTS</span></span>

## <span data-ttu-id="23f98-139">상속자</span><span class="sxs-lookup"><span data-stu-id="23f98-139">NOTES</span></span>

## <span data-ttu-id="23f98-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="23f98-140">RELATED LINKS</span></span>

[<span data-ttu-id="23f98-141">다운로드-Add-azurevm</span><span class="sxs-lookup"><span data-stu-id="23f98-141">Get-AzureVM</span></span>](./Get-AzureVM.md)

[<span data-ttu-id="23f98-142">뉴욕</span><span class="sxs-lookup"><span data-stu-id="23f98-142">New-AzureVM</span></span>](./New-AzureVM.md)

[<span data-ttu-id="23f98-143">새로운 AzureVMConfig</span><span class="sxs-lookup"><span data-stu-id="23f98-143">New-AzureVMConfig</span></span>](./New-AzureVMConfig.md)

[<span data-ttu-id="23f98-144">제거-Add-azurevm</span><span class="sxs-lookup"><span data-stu-id="23f98-144">Remove-AzureVM</span></span>](./Remove-AzureVM.md)

[<span data-ttu-id="23f98-145">-Add-azurevm 다시 시작</span><span class="sxs-lookup"><span data-stu-id="23f98-145">Restart-AzureVM</span></span>](./Restart-AzureVM.md)

[<span data-ttu-id="23f98-146">Set-AzureVMSize</span><span class="sxs-lookup"><span data-stu-id="23f98-146">Set-AzureVMSize</span></span>](./Set-AzureVMSize.md)

[<span data-ttu-id="23f98-147">시작-Add-azurevm</span><span class="sxs-lookup"><span data-stu-id="23f98-147">Start-AzureVM</span></span>](./Start-AzureVM.md)

[<span data-ttu-id="23f98-148">-Add-azurevm</span><span class="sxs-lookup"><span data-stu-id="23f98-148">Stop-AzureVM</span></span>](./Stop-AzureVM.md)


