---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azimageosdisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzImageOsDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzImageOsDisk.md
ms.openlocfilehash: 5bc92ea5aa49cb97be457fd937c7b9deb492bb0e
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93876905"
---
# <span data-ttu-id="0a0fd-101">Set-AzImageOsDisk</span><span class="sxs-lookup"><span data-stu-id="0a0fd-101">Set-AzImageOsDisk</span></span>

## <span data-ttu-id="0a0fd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0a0fd-102">SYNOPSIS</span></span>
<span data-ttu-id="0a0fd-103">Image 개체에서 운영 체제 디스크 속성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0a0fd-103">Sets the operating system disk properties on an image object.</span></span>

## <span data-ttu-id="0a0fd-104">구문과</span><span class="sxs-lookup"><span data-stu-id="0a0fd-104">SYNTAX</span></span>

```
Set-AzImageOsDisk [-Image] <PSImage> [[-OsType] <OperatingSystemTypes>]
 [[-OsState] <OperatingSystemStateTypes>] [[-BlobUri] <String>] [-Caching <CachingTypes>] [-DiskSizeGB <Int32>]
 [-StorageAccountType <StorageAccountTypes>] [-SnapshotId <String>] [-ManagedDiskId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0a0fd-105">설명은</span><span class="sxs-lookup"><span data-stu-id="0a0fd-105">DESCRIPTION</span></span>
<span data-ttu-id="0a0fd-106">**AzImageOsDisk** cmdlet은 image 개체에 대 한 운영 체제 디스크 속성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0a0fd-106">The **Set-AzImageOsDisk** cmdlet sets the operating system disk properties on an image object.</span></span>

## <span data-ttu-id="0a0fd-107">예제의</span><span class="sxs-lookup"><span data-stu-id="0a0fd-107">EXAMPLES</span></span>

### <span data-ttu-id="0a0fd-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="0a0fd-108">Example 1</span></span>
```
PS C:\> $imageConfig = New-AzImageConfig -Location 'West US';
PS C:\> $osDiskVhdUri = "https://contoso.blob.core.windows.net/test/os.vhd"
PS C:\> $dataDiskVhdUri1 = "https://contoso.blob.core.windows.net/test/data1.vhd"
PS C:\> $dataDiskVhdUri2 = "https://contoso.blob.core.windows.net/test/data2.vhd"
PS C:\> Set-AzImageOsDisk -Image $imageConfig -OsType 'Windows' -OsState 'Generalized' -BlobUri $osDiskVhdUri;
PS C:\> Add-AzImageDataDisk -Image $imageConfig -Lun 1 -BlobUri $dataDiskVhdUri1;
PS C:\> Add-AzImageDataDisk -Image $imageConfig -Lun 2 -BlobUri $dataDiskVhdUri2;
PS C:\> New-AzImage -Image $imageConfig -ImageName 'ImageName01' -ResourceGroupName 'ResourceGroup01';
```

<span data-ttu-id="0a0fd-109">첫 번째 명령은 image 개체를 만든 다음 $imageConfig 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="0a0fd-109">The first command creates an image object, and then stores it in the $imageConfig variable.</span></span>

<span data-ttu-id="0a0fd-110">다음 세 개의 명령은 os 디스크의 경로와 두 개의 데이터 디스크를 $osDiskVhdUri, $dataDiskVhdUri 1 및 $dataDiskVhdUri 2 변수에 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="0a0fd-110">The next three commands assign paths of os disk and two data disks to the $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2 variables.</span></span>
<span data-ttu-id="0a0fd-111">이 방법은 다음 명령에 대 한 읽기 전용입니다.</span><span class="sxs-lookup"><span data-stu-id="0a0fd-111">This approach is only for readability of the following commands.</span></span>

<span data-ttu-id="0a0fd-112">다음 세 개의 명령은 각각 os 디스크와 두 개의 데이터 디스크를 $imageConfig에 저장 된 이미지에 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="0a0fd-112">The next three commands each adds an os disk and two data disks to the image stored in $imageConfig.</span></span>
<span data-ttu-id="0a0fd-113">각 디스크의 URI는 $osDiskVhdUri, $dataDiskVhdUri 1 및 $dataDiskVhdUri 2에 저장 됩니다.</span><span class="sxs-lookup"><span data-stu-id="0a0fd-113">The URI of each disk is stored in $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2.</span></span>

<span data-ttu-id="0a0fd-114">마지막 명령은 리소스 그룹 ' ResourceGroup01 '에 ' ImageName01 ' 이미지를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="0a0fd-114">The final command creates an image named 'ImageName01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="0a0fd-115">변수</span><span class="sxs-lookup"><span data-stu-id="0a0fd-115">PARAMETERS</span></span>

### <span data-ttu-id="0a0fd-116">-BlobUri</span><span class="sxs-lookup"><span data-stu-id="0a0fd-116">-BlobUri</span></span>
<span data-ttu-id="0a0fd-117">Blob의 Uri를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0a0fd-117">Specifies the Uri of the blob.</span></span>

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

### <span data-ttu-id="0a0fd-118">-캐싱</span><span class="sxs-lookup"><span data-stu-id="0a0fd-118">-Caching</span></span>
<span data-ttu-id="0a0fd-119">디스크의 캐싱 모드를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0a0fd-119">Specifies the caching mode of the disk.</span></span>

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

### <span data-ttu-id="0a0fd-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0a0fd-120">-DefaultProfile</span></span>
<span data-ttu-id="0a0fd-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="0a0fd-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a0fd-122">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="0a0fd-122">-DiskSizeGB</span></span>
<span data-ttu-id="0a0fd-123">디스크 크기 (GB)를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0a0fd-123">Specifies the size of the disk in GB.</span></span>

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

### <span data-ttu-id="0a0fd-124">-이미지</span><span class="sxs-lookup"><span data-stu-id="0a0fd-124">-Image</span></span>
<span data-ttu-id="0a0fd-125">로컬 이미지 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0a0fd-125">Specifies a local image object.</span></span>

```yaml
Type: PSImage
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0a0fd-126">-ManagedDiskId</span><span class="sxs-lookup"><span data-stu-id="0a0fd-126">-ManagedDiskId</span></span>
<span data-ttu-id="0a0fd-127">관리 디스크의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0a0fd-127">Specifies the ID of a managed disk.</span></span>

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

### <span data-ttu-id="0a0fd-128">-OsState</span><span class="sxs-lookup"><span data-stu-id="0a0fd-128">-OsState</span></span>
<span data-ttu-id="0a0fd-129">OS 상태를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0a0fd-129">Specifies the OS state.</span></span>

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

### <span data-ttu-id="0a0fd-130">-OsType</span><span class="sxs-lookup"><span data-stu-id="0a0fd-130">-OsType</span></span>
<span data-ttu-id="0a0fd-131">OS 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0a0fd-131">Specifies the OS type.</span></span>

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

### <span data-ttu-id="0a0fd-132">-SnapshotId</span><span class="sxs-lookup"><span data-stu-id="0a0fd-132">-SnapshotId</span></span>
<span data-ttu-id="0a0fd-133">스냅숏의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0a0fd-133">Specifies the ID of a snapshot.</span></span>

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

### <span data-ttu-id="0a0fd-134">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="0a0fd-134">-StorageAccountType</span></span>
<span data-ttu-id="0a0fd-135">Os 이미지 디스크의 저장소 계정 유형</span><span class="sxs-lookup"><span data-stu-id="0a0fd-135">The Storage Account type of Os Image Disk</span></span>

```yaml
Type: StorageAccountTypes
Parameter Sets: (All)
Aliases: 
Accepted values: StandardLRS, PremiumLRS

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a0fd-136">-확인</span><span class="sxs-lookup"><span data-stu-id="0a0fd-136">-Confirm</span></span>
<span data-ttu-id="0a0fd-137">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="0a0fd-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0a0fd-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0a0fd-138">-WhatIf</span></span>
<span data-ttu-id="0a0fd-139">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="0a0fd-139">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0a0fd-140">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0a0fd-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0a0fd-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a0fd-141">CommonParameters</span></span>
<span data-ttu-id="0a0fd-142">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="0a0fd-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a0fd-143">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0a0fd-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a0fd-144">입력</span><span class="sxs-lookup"><span data-stu-id="0a0fd-144">INPUTS</span></span>

### <span data-ttu-id="0a0fd-145">Microsoft. 관리. 이미지</span><span class="sxs-lookup"><span data-stu-id="0a0fd-145">Microsoft.Azure.Management.Compute.Models.Image</span></span>
<span data-ttu-id="0a0fd-146">시스템 Null 허용 `1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]
System.Nullable` 1 [[[OperatingSystemStateTypes, microsoft azure. 14.0.0.0, Version =, Culture = 중립, publickeytoken = 31bf3856ad364e35]] system. 문자열 시스템. Null 허용 `1[[Microsoft.Azure.Management.Compute.Models.CachingTypes, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]
System.Nullable` 1 [[[System. Int32, Mscorlib, Version = 4.0.0.0, culture = 중립, publickeytoken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="0a0fd-146">System.Nullable`1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]
System.Nullable`1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemStateTypes, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]] System.String System.Nullable`1[[Microsoft.Azure.Management.Compute.Models.CachingTypes, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]
System.Nullable`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="0a0fd-147">출력</span><span class="sxs-lookup"><span data-stu-id="0a0fd-147">OUTPUTS</span></span>

### <span data-ttu-id="0a0fd-148">Microsoft. 관리. 이미지</span><span class="sxs-lookup"><span data-stu-id="0a0fd-148">Microsoft.Azure.Management.Compute.Models.Image</span></span>

## <span data-ttu-id="0a0fd-149">상속자</span><span class="sxs-lookup"><span data-stu-id="0a0fd-149">NOTES</span></span>

## <span data-ttu-id="0a0fd-150">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0a0fd-150">RELATED LINKS</span></span>

