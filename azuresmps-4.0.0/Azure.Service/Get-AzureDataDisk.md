---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 2A8BE3EB-4929-4B40-82EA-5434C09A5251
online version: ''
schema: 2.0.0
ms.openlocfilehash: 1974de3f5c4bf39aa32100e67bb04642ebcfe3da
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045651"
---
# <span data-ttu-id="d8065-101">Get-AzureDataDisk</span><span class="sxs-lookup"><span data-stu-id="d8065-101">Get-AzureDataDisk</span></span>

## <span data-ttu-id="d8065-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d8065-102">SYNOPSIS</span></span>
<span data-ttu-id="d8065-103">Azure 데이터 디스크를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d8065-103">Gets Azure data disks.</span></span>

## <span data-ttu-id="d8065-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d8065-104">SYNTAX</span></span>

```
Get-AzureDataDisk [[-Lun] <Int32>] -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="d8065-105">설명은</span><span class="sxs-lookup"><span data-stu-id="d8065-105">DESCRIPTION</span></span>
<span data-ttu-id="d8065-106">**Get-AzureDataDisk** Cmdlet은 Azure 가상 컴퓨터의 데이터 디스크를 나타내는 개체를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d8065-106">The **Get-AzureDataDisk** cmdlet gets an object that represents the data disks on an Azure virtual machine.</span></span>
<span data-ttu-id="d8065-107">특정 데이터 디스크 개체를 가져오려면 디스크의 LUN (논리 단위 번호)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d8065-107">To get a specific data disk object, specify the logical unit number (LUN) of the disk.</span></span>

## <span data-ttu-id="d8065-108">예제의</span><span class="sxs-lookup"><span data-stu-id="d8065-108">EXAMPLES</span></span>

### <span data-ttu-id="d8065-109">예제 1: 가상 컴퓨터용 모든 데이터 디스크 가져오기</span><span class="sxs-lookup"><span data-stu-id="d8065-109">Example 1: Get all data disks for a virtual machine</span></span>
```
PS C:\> Get-AzureVM "ContosoService" -Name "VirtualMachine07" | Get-AzureDataDisk
```

<span data-ttu-id="d8065-110">이 명령은 VirtualMachine07 cmdlet을 사용 하 여 ContosoService 이라는 서비스의 가상 컴퓨터 (이름 = **)** 를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d8065-110">This command gets the virtual machine named VirtualMachine07 in the service named ContosoService by using the **Get-AzureVM** cmdlet.</span></span>
<span data-ttu-id="d8065-111">이 명령은 파이프라인 연산자를 사용 하 여 가상 컴퓨터를 현재 cmdlet에 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="d8065-111">The command passes the virtual machine to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="d8065-112">현재 cmdlet은이 가상 컴퓨터에 대 한 모든 데이터 디스크를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d8065-112">The current cmdlet gets all the data disks for this virtual machine.</span></span>

### <span data-ttu-id="d8065-113">예제 2: vituralvirtual machinevirtual 용 특정 데이터 디스크 가져오기</span><span class="sxs-lookup"><span data-stu-id="d8065-113">Example 2: Get a specific data disk for a vituralvirtual machinevirtual</span></span>
```
PS C:\> Get-AzureVM "ContosoService" -Name "VirtualMachine07" | Get-AzureDataDisk -LUN 2
```

<span data-ttu-id="d8065-114">이 명령은 ContosoService 이라는 서비스에서 VirtualMachine07 이라는 가상 컴퓨터를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d8065-114">This command gets the virtual machine named VirtualMachine07 in the service named ContosoService.</span></span>
<span data-ttu-id="d8065-115">명령이 가상 컴퓨터를 현재 cmdlet에 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="d8065-115">The command passes the virtual machine to the current cmdlet.</span></span>
<span data-ttu-id="d8065-116">현재 cmdlet은 LUN 2가 있는 데이터 디스크를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d8065-116">The current cmdlet gets the data disk that has the LUN 2.</span></span>

## <span data-ttu-id="d8065-117">변수</span><span class="sxs-lookup"><span data-stu-id="d8065-117">PARAMETERS</span></span>

### <span data-ttu-id="d8065-118">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="d8065-118">-InformationAction</span></span>
<span data-ttu-id="d8065-119">이 cmdlet이 정보 이벤트에 응답 하는 방법을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d8065-119">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="d8065-120">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="d8065-120">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="d8065-121">하기로</span><span class="sxs-lookup"><span data-stu-id="d8065-121">Continue</span></span>
- <span data-ttu-id="d8065-122">숨기기</span><span class="sxs-lookup"><span data-stu-id="d8065-122">Ignore</span></span>
- <span data-ttu-id="d8065-123">Inquire</span><span class="sxs-lookup"><span data-stu-id="d8065-123">Inquire</span></span>
- <span data-ttu-id="d8065-124">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="d8065-124">SilentlyContinue</span></span>
- <span data-ttu-id="d8065-125">중지가</span><span class="sxs-lookup"><span data-stu-id="d8065-125">Stop</span></span>
- <span data-ttu-id="d8065-126">대기</span><span class="sxs-lookup"><span data-stu-id="d8065-126">Suspend</span></span>

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

### <span data-ttu-id="d8065-127">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="d8065-127">-InformationVariable</span></span>
<span data-ttu-id="d8065-128">정보 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d8065-128">Specifies an information variable.</span></span>

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

### <span data-ttu-id="d8065-129">-Lun</span><span class="sxs-lookup"><span data-stu-id="d8065-129">-Lun</span></span>
<span data-ttu-id="d8065-130">가상 컴퓨터의 데이터 드라이브에 대 한 LUN을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d8065-130">Specifies the LUN for the data drive in the virtual machine.</span></span>
<span data-ttu-id="d8065-131">유효한 값은 0 ~ 15입니다.</span><span class="sxs-lookup"><span data-stu-id="d8065-131">Valid values are: 0 through 15.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8065-132">-프로필</span><span class="sxs-lookup"><span data-stu-id="d8065-132">-Profile</span></span>
<span data-ttu-id="d8065-133">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d8065-133">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="d8065-134">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="d8065-134">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="d8065-135">-VM</span><span class="sxs-lookup"><span data-stu-id="d8065-135">-VM</span></span>
<span data-ttu-id="d8065-136">이 cmdlet에서 데이터 디스크를 가져오는 가상 컴퓨터 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d8065-136">Specifies the virtual machine object for which this cmdlet gets data disks.</span></span>
<span data-ttu-id="d8065-137">가상 컴퓨터 개체를 가져오려면 **get-help** cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="d8065-137">To obtain a virtual machine object, use the **Get-AzureVM** cmdlet.</span></span>

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

### <span data-ttu-id="d8065-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8065-138">CommonParameters</span></span>
<span data-ttu-id="d8065-139">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d8065-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8065-140">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d8065-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8065-141">입력</span><span class="sxs-lookup"><span data-stu-id="d8065-141">INPUTS</span></span>

## <span data-ttu-id="d8065-142">출력</span><span class="sxs-lookup"><span data-stu-id="d8065-142">OUTPUTS</span></span>

## <span data-ttu-id="d8065-143">상속자</span><span class="sxs-lookup"><span data-stu-id="d8065-143">NOTES</span></span>

## <span data-ttu-id="d8065-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d8065-144">RELATED LINKS</span></span>

[<span data-ttu-id="d8065-145">-AzureDataDisk 추가</span><span class="sxs-lookup"><span data-stu-id="d8065-145">Add-AzureDataDisk</span></span>](./Add-AzureDataDisk.md)

[<span data-ttu-id="d8065-146">다운로드-Add-azurevm</span><span class="sxs-lookup"><span data-stu-id="d8065-146">Get-AzureVM</span></span>](./Get-AzureVM.md)

[<span data-ttu-id="d8065-147">-AzureDataDisk 제거</span><span class="sxs-lookup"><span data-stu-id="d8065-147">Remove-AzureDataDisk</span></span>](./Remove-AzureDataDisk.md)

[<span data-ttu-id="d8065-148">Set AzureDataDisk</span><span class="sxs-lookup"><span data-stu-id="d8065-148">Set-AzureDataDisk</span></span>](./Set-AzureDataDisk.md)


