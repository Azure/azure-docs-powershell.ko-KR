---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: F16BCE0C-1F2C-4FB7-972D-28BE3CCD96D9
online version: ''
schema: 2.0.0
ms.openlocfilehash: dc41efa1901debf2efabf66f8d27f00da7eafe5f
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045511"
---
# <span data-ttu-id="06317-101">New-AzureStorSimpleVirtualDevice</span><span class="sxs-lookup"><span data-stu-id="06317-101">New-AzureStorSimpleVirtualDevice</span></span>

## <span data-ttu-id="06317-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="06317-102">SYNOPSIS</span></span>
<span data-ttu-id="06317-103">가상 StorSimple 장치를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="06317-103">Creates a virtual StorSimple device.</span></span>

## <span data-ttu-id="06317-104">구문과</span><span class="sxs-lookup"><span data-stu-id="06317-104">SYNTAX</span></span>

### <span data-ttu-id="06317-105">CreateNewStorageAccount</span><span class="sxs-lookup"><span data-stu-id="06317-105">CreateNewStorageAccount</span></span>
```
New-AzureStorSimpleVirtualDevice -VirtualDeviceName <String> -VirtualNetworkName <String> -SubNetName <String>
 [-StorageAccountName <String>] [-CreateNewStorageAccount] [-PersistAzureVMOnFailrue]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="06317-106">UseExistingStorageAccount</span><span class="sxs-lookup"><span data-stu-id="06317-106">UseExistingStorageAccount</span></span>
```
New-AzureStorSimpleVirtualDevice -VirtualDeviceName <String> -VirtualNetworkName <String> -SubNetName <String>
 -StorageAccountName <String> [-PersistAzureVMOnFailrue] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="06317-107">설명은</span><span class="sxs-lookup"><span data-stu-id="06317-107">DESCRIPTION</span></span>
<span data-ttu-id="06317-108">**AzureStorSimpleVirtualDevice** cmdlet은 가상 StorSimple 장치를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="06317-108">The **New-AzureStorSimpleVirtualDevice** cmdlet creates a virtual StorSimple device.</span></span>
<span data-ttu-id="06317-109">장치에 대 한 디바이스 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="06317-109">Specify a device name for the device.</span></span>
<span data-ttu-id="06317-110">동일한 구독에서 가상 네트워크에 대 한 가상 네트워크 및 서브넷 세부 정보를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="06317-110">Specify virtual network and subnet details for the virtual network in the same subscription.</span></span>
<span data-ttu-id="06317-111">Geo는 StorSimple 리소스가 생성 되는 geo와 일치 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="06317-111">The geo should match the geo in which the StorSimple resource is created.</span></span>
<span data-ttu-id="06317-112">이 가상 장치에 대 한 기존 저장소 계정을 사용 하려면 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="06317-112">To use an existing storage account for this virtual device, specify the name.</span></span>
<span data-ttu-id="06317-113">이 가상 장치에 대 한 새 저장소 계정을 만들려면 *Storageaccountname* 및 *CreateNewStorageAccount* 매개 변수를 둘 다 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="06317-113">To create a new storage account for this virtual device, specify both the *StorageAccountName* and the *CreateNewStorageAccount* parameters.</span></span>

## <span data-ttu-id="06317-114">예제의</span><span class="sxs-lookup"><span data-stu-id="06317-114">EXAMPLES</span></span>

### <span data-ttu-id="06317-115">예제 1: 새 계정 및 기존 네트워크를 사용 하 여 가상 장치 만들기</span><span class="sxs-lookup"><span data-stu-id="06317-115">Example 1: Create a virtual device with a new account and an existing network</span></span>
```
PS C:\>New-AzureStorSimpleVirtualDevice -VirtualDeviceName "Contosodevice02" -VirtualNetworkName "Saas2vpn" -SubNetName "TenantSubnet" -StorageAccountName "AzureTenant04" -CreateNewStorageAccount
64e4c564-b0ac-44b0-afb4-adf28ac24ad0
VERBOSE: The create job is triggered successfully. Please use the command Get-AzureStorSimpleJob -InstanceId 64e4c564-b0ac-44b0-afb4-adf28ac24ad0 for tracking the job's status
```

<span data-ttu-id="06317-116">이 명령은 새 저장소 계정과 기존 가상 네트워크를 사용 하는 가상 장치를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="06317-116">This command creates a virtual device that uses a new storage account and an existing virtual network.</span></span>

### <span data-ttu-id="06317-117">예제 2: 기존 계정 및 가상 네트워크를 사용 하 여 가상 장치 만들기</span><span class="sxs-lookup"><span data-stu-id="06317-117">Example 2: Create a virtual device with an existing account and virtual network</span></span>
```
PS C:\>New-AzureStorSimpleVirtualDevice -VirtualDeviceName "ContosoDevice07" -VirtualNetworkName "Saas2vpn" -SubNetName TenantSubnet -StorageAccountName azurecisbvtdnd
2a18a3b7-1ec6-481d-b95d-66ba8f67ceaf
VERBOSE: The create job is triggered successfully. Please use the command Get-AzureStorSimpleJob -InstanceId 2a18a3b7-1ec6-481d-b95d-66ba8f67ceaf for tracking the job's status
```

<span data-ttu-id="06317-118">이 명령은 기존 저장소 계정과 기존 가상 네트워크를 사용 하는 가상 장치를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="06317-118">This command creates a virtual device that uses an existing storage account and an existing virtual network.</span></span>

## <span data-ttu-id="06317-119">변수</span><span class="sxs-lookup"><span data-stu-id="06317-119">PARAMETERS</span></span>

### <span data-ttu-id="06317-120">-CreateNewStorageAccount</span><span class="sxs-lookup"><span data-stu-id="06317-120">-CreateNewStorageAccount</span></span>
<span data-ttu-id="06317-121">이 cmdlet이 새 저장소 계정을 생성 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="06317-121">Indicates that this cmdlet creates a new storage account.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: CreateNewStorageAccount
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06317-122">-PersistAzureVMOnFailrue</span><span class="sxs-lookup"><span data-stu-id="06317-122">-PersistAzureVMOnFailrue</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06317-123">-프로필</span><span class="sxs-lookup"><span data-stu-id="06317-123">-Profile</span></span>
<span data-ttu-id="06317-124">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="06317-124">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="06317-125">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="06317-125">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="06317-126">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="06317-126">-StorageAccountName</span></span>
<span data-ttu-id="06317-127">저장소 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="06317-127">Specifies the name of a storage account.</span></span>

```yaml
Type: String
Parameter Sets: CreateNewStorageAccount
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: UseExistingStorageAccount
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06317-128">-SubNetName</span><span class="sxs-lookup"><span data-stu-id="06317-128">-SubNetName</span></span>
<span data-ttu-id="06317-129">가상 서브넷의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="06317-129">Specifies the name of a virtual subnet.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06317-130">-VirtualDeviceName 이름</span><span class="sxs-lookup"><span data-stu-id="06317-130">-VirtualDeviceName</span></span>
<span data-ttu-id="06317-131">가상 디바이스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="06317-131">Specifies a name for the virtual device.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06317-132">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="06317-132">-VirtualNetworkName</span></span>
<span data-ttu-id="06317-133">가상 네트워크의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="06317-133">Specifies the name of a virtual network.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: VNetName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06317-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06317-134">CommonParameters</span></span>
<span data-ttu-id="06317-135">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="06317-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06317-136">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="06317-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06317-137">입력</span><span class="sxs-lookup"><span data-stu-id="06317-137">INPUTS</span></span>

## <span data-ttu-id="06317-138">출력</span><span class="sxs-lookup"><span data-stu-id="06317-138">OUTPUTS</span></span>

### <span data-ttu-id="06317-139">이름</span><span class="sxs-lookup"><span data-stu-id="06317-139">String</span></span>
<span data-ttu-id="06317-140">이 cmdlet은 가상 장치를 만드는 작업의 ID를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="06317-140">This cmdlet returns the ID of the job that creates the virtual device.</span></span>
<span data-ttu-id="06317-141">이 ID를 사용 하 여 Get-AzureStorSimpleJob cmdlet을 사용 하 여 진행률을 추적할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="06317-141">You can use this ID to track the progress using the Get-AzureStorSimpleJob cmdlet.</span></span>

## <span data-ttu-id="06317-142">상속자</span><span class="sxs-lookup"><span data-stu-id="06317-142">NOTES</span></span>

## <span data-ttu-id="06317-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="06317-143">RELATED LINKS</span></span>

[<span data-ttu-id="06317-144">Get-AzureStorSimpleJob</span><span class="sxs-lookup"><span data-stu-id="06317-144">Get-AzureStorSimpleJob</span></span>](./Get-AzureStorSimpleJob.md)

[<span data-ttu-id="06317-145">Set-AzureStorSimpleVirtualDevice</span><span class="sxs-lookup"><span data-stu-id="06317-145">Set-AzureStorSimpleVirtualDevice</span></span>](./Set-AzureStorSimpleVirtualDevice.md)


