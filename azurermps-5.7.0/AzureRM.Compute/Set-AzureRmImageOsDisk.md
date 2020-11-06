---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmImageOsDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmImageOsDisk.md
ms.openlocfilehash: 8deb191a6a26e4fb0001a1cbb78540460256dd97
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93525300"
---
# <span data-ttu-id="9fd81-101">Set-AzureRmImageOsDisk</span><span class="sxs-lookup"><span data-stu-id="9fd81-101">Set-AzureRmImageOsDisk</span></span>

## <span data-ttu-id="9fd81-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9fd81-102">SYNOPSIS</span></span>
<span data-ttu-id="9fd81-103">Image 개체에서 운영 체제 디스크 속성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9fd81-103">Sets the operating system disk properties on an image object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9fd81-104">구문과</span><span class="sxs-lookup"><span data-stu-id="9fd81-104">SYNTAX</span></span>

```
Set-AzureRmImageOsDisk [-Image] <Image> [[-OsType] <OperatingSystemTypes>]
 [[-OsState] <OperatingSystemStateTypes>] [[-BlobUri] <String>] [-Caching <CachingTypes>] [-DiskSizeGB <Int32>]
 [-StorageAccountType <StorageAccountTypes>] [-SnapshotId <String>] [-ManagedDiskId <String>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9fd81-105">설명은</span><span class="sxs-lookup"><span data-stu-id="9fd81-105">DESCRIPTION</span></span>
<span data-ttu-id="9fd81-106">**AzureRmImageOsDisk** cmdlet은 image 개체에 대 한 운영 체제 디스크 속성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9fd81-106">The **Set-AzureRmImageOsDisk** cmdlet sets the operating system disk properties on an image object.</span></span>

## <span data-ttu-id="9fd81-107">예제의</span><span class="sxs-lookup"><span data-stu-id="9fd81-107">EXAMPLES</span></span>

### <span data-ttu-id="9fd81-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="9fd81-108">Example 1</span></span>
```
PS C:\> $imageConfig = New-AzureRmImageConfig -Location 'West US';
PS C:\> $osDiskVhdUri = "https://contoso.blob.core.windows.net/test/os.vhd"
PS C:\> $dataDiskVhdUri1 = "https://contoso.blob.core.windows.net/test/data1.vhd"
PS C:\> $dataDiskVhdUri2 = "https://contoso.blob.core.windows.net/test/data2.vhd"
PS C:\> Set-AzureRmImageOsDisk -Image $imageConfig -OsType 'Windows' -OsState 'Generalized' -BlobUri $osDiskVhdUri;
PS C:\> Add-AzureRmImageDataDisk -Image $imageConfig -Lun 1 -BlobUri $dataDiskVhdUri1;
PS C:\> Add-AzureRmImageDataDisk -Image $imageConfig -Lun 2 -BlobUri $dataDiskVhdUri2;
PS C:\> New-AzureRmImage -Image $imageConfig -ImageName 'ImageName01' -ResourceGroupName 'ResourceGroup01';
```

<span data-ttu-id="9fd81-109">첫 번째 명령은 image 개체를 만든 다음 $imageConfig 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="9fd81-109">The first command creates an image object, and then stores it in the $imageConfig variable.</span></span>

<span data-ttu-id="9fd81-110">다음 세 개의 명령은 os 디스크의 경로와 두 개의 데이터 디스크를 $osDiskVhdUri, $dataDiskVhdUri 1 및 $dataDiskVhdUri 2 변수에 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="9fd81-110">The next three commands assign paths of os disk and two data disks to the $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2 variables.</span></span>
<span data-ttu-id="9fd81-111">이 방법은 다음 명령에 대 한 읽기 전용입니다.</span><span class="sxs-lookup"><span data-stu-id="9fd81-111">This approach is only for readability of the following commands.</span></span>

<span data-ttu-id="9fd81-112">다음 세 개의 명령은 각각 os 디스크와 두 개의 데이터 디스크를 $imageConfig에 저장 된 이미지에 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="9fd81-112">The next three commands each adds an os disk and two data disks to the image stored in $imageConfig.</span></span>
<span data-ttu-id="9fd81-113">각 디스크의 URI는 $osDiskVhdUri, $dataDiskVhdUri 1 및 $dataDiskVhdUri 2에 저장 됩니다.</span><span class="sxs-lookup"><span data-stu-id="9fd81-113">The URI of each disk is stored in $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2.</span></span>

<span data-ttu-id="9fd81-114">마지막 명령은 리소스 그룹 ' ResourceGroup01 '에 ' ImageName01 ' 이미지를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="9fd81-114">The final command creates an image named 'ImageName01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="9fd81-115">변수</span><span class="sxs-lookup"><span data-stu-id="9fd81-115">PARAMETERS</span></span>

### <span data-ttu-id="9fd81-116">-BlobUri</span><span class="sxs-lookup"><span data-stu-id="9fd81-116">-BlobUri</span></span>
<span data-ttu-id="9fd81-117">Blob의 Uri를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9fd81-117">Specifies the Uri of the blob.</span></span>

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

### <span data-ttu-id="9fd81-118">-캐싱</span><span class="sxs-lookup"><span data-stu-id="9fd81-118">-Caching</span></span>
<span data-ttu-id="9fd81-119">디스크의 캐싱 모드를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9fd81-119">Specifies the caching mode of the disk.</span></span>

```yaml
Type: CachingTypes
Parameter Sets: (All)
Aliases: 
Accepted values: None, ReadOnly, ReadWrite

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9fd81-120">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="9fd81-120">-DiskSizeGB</span></span>
<span data-ttu-id="9fd81-121">디스크 크기 (GB)를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9fd81-121">Specifies the size of the disk in GB.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9fd81-122">-이미지</span><span class="sxs-lookup"><span data-stu-id="9fd81-122">-Image</span></span>
<span data-ttu-id="9fd81-123">로컬 이미지 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9fd81-123">Specifies a local image object.</span></span>

```yaml
Type: Image
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9fd81-124">-ManagedDiskId</span><span class="sxs-lookup"><span data-stu-id="9fd81-124">-ManagedDiskId</span></span>
<span data-ttu-id="9fd81-125">관리 디스크의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9fd81-125">Specifies the ID of a managed disk.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9fd81-126">-OsState</span><span class="sxs-lookup"><span data-stu-id="9fd81-126">-OsState</span></span>
<span data-ttu-id="9fd81-127">OS 상태를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9fd81-127">Specifies the OS state.</span></span>

```yaml
Type: OperatingSystemStateTypes
Parameter Sets: (All)
Aliases: 
Accepted values: Generalized, Specialized

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9fd81-128">-OsType</span><span class="sxs-lookup"><span data-stu-id="9fd81-128">-OsType</span></span>
<span data-ttu-id="9fd81-129">OS 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9fd81-129">Specifies the OS type.</span></span>

```yaml
Type: OperatingSystemTypes
Parameter Sets: (All)
Aliases: 
Accepted values: Windows, Linux

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9fd81-130">-SnapshotId</span><span class="sxs-lookup"><span data-stu-id="9fd81-130">-SnapshotId</span></span>
<span data-ttu-id="9fd81-131">스냅숏의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9fd81-131">Specifies the ID of a snapshot.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9fd81-132">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="9fd81-132">-StorageAccountType</span></span>
<span data-ttu-id="9fd81-133">Os 이미지 디스크의 저장소 계정 유형</span><span class="sxs-lookup"><span data-stu-id="9fd81-133">The Storage Account type of Os Image Disk</span></span>

```yaml
Type: StorageAccountTypes
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9fd81-134">-확인</span><span class="sxs-lookup"><span data-stu-id="9fd81-134">-Confirm</span></span>
<span data-ttu-id="9fd81-135">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="9fd81-135">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fd81-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9fd81-136">-WhatIf</span></span>
<span data-ttu-id="9fd81-137">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="9fd81-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9fd81-138">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9fd81-138">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fd81-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9fd81-139">CommonParameters</span></span>
<span data-ttu-id="9fd81-140">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="9fd81-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9fd81-141">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9fd81-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9fd81-142">입력</span><span class="sxs-lookup"><span data-stu-id="9fd81-142">INPUTS</span></span>

### <span data-ttu-id="9fd81-143">Microsoft. 관리. 이미지</span><span class="sxs-lookup"><span data-stu-id="9fd81-143">Microsoft.Azure.Management.Compute.Models.Image</span></span>
<span data-ttu-id="9fd81-144">시스템 Null 허용 `1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]
System.Nullable` 1 [[[OperatingSystemStateTypes, microsoft azure. 14.0.0.0, Version =, Culture = 중립, publickeytoken = 31bf3856ad364e35]] system. 문자열 시스템. Null 허용 `1[[Microsoft.Azure.Management.Compute.Models.CachingTypes, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]
System.Nullable` 1 [[[System. Int32, Mscorlib, Version = 4.0.0.0, culture = 중립, publickeytoken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="9fd81-144">System.Nullable`1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]
System.Nullable`1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemStateTypes, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]] System.String System.Nullable`1[[Microsoft.Azure.Management.Compute.Models.CachingTypes, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]
System.Nullable`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="9fd81-145">출력</span><span class="sxs-lookup"><span data-stu-id="9fd81-145">OUTPUTS</span></span>

### <span data-ttu-id="9fd81-146">Microsoft. 관리. 이미지</span><span class="sxs-lookup"><span data-stu-id="9fd81-146">Microsoft.Azure.Management.Compute.Models.Image</span></span>

## <span data-ttu-id="9fd81-147">상속자</span><span class="sxs-lookup"><span data-stu-id="9fd81-147">NOTES</span></span>

## <span data-ttu-id="9fd81-148">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9fd81-148">RELATED LINKS</span></span>

