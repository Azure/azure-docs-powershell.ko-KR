---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/set-azurermdiskimagereference
schema: 2.0.0
ms.openlocfilehash: cd0a66d8f8d777df9a8ebc3791643234f0d15fb0
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93881946"
---
# <span data-ttu-id="b62ee-101">Set-AzureRmDiskImageReference</span><span class="sxs-lookup"><span data-stu-id="b62ee-101">Set-AzureRmDiskImageReference</span></span>

## <span data-ttu-id="b62ee-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b62ee-102">SYNOPSIS</span></span>
<span data-ttu-id="b62ee-103">Disk 개체에 대 한 이미지 참조 속성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b62ee-103">Sets the image reference properties on a disk object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b62ee-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b62ee-104">SYNTAX</span></span>

```
Set-AzureRmDiskImageReference [-Disk] <PSDisk> [[-Id] <String>] [[-Lun] <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b62ee-105">설명은</span><span class="sxs-lookup"><span data-stu-id="b62ee-105">DESCRIPTION</span></span>
<span data-ttu-id="b62ee-106">**Set-AzureRmDiskImageReference** cmdlet은 disk 개체의 이미지 참조 속성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b62ee-106">The **Set-AzureRmDiskImageReference** cmdlet sets the image reference properties on a disk object.</span></span>

## <span data-ttu-id="b62ee-107">예제의</span><span class="sxs-lookup"><span data-stu-id="b62ee-107">EXAMPLES</span></span>

### <span data-ttu-id="b62ee-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="b62ee-108">Example 1</span></span>
```
PS C:\> $diskconfig = New-AzureRmDiskConfig -DiskSizeGB 10 -AccountType PremiumLRS -OsType Windows -CreateOption FromImage;
PS C:\> $image = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.Compute/images/TestImage123';        
PS C:\> $diskconfig = Set-AzureRmDiskImageReference -Disk $diskconfig -Id $image -Lun 0;
PS C:\> New-AzureRmDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Disk $diskconfig;
```

<span data-ttu-id="b62ee-109">첫 번째 명령은 Premium_LRS 저장소 계정 유형의 10GB 크기의 로컬 디스크 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b62ee-109">The first command creates a local disk object with size 10GB in Premium_LRS storage account type.</span></span>  <span data-ttu-id="b62ee-110">Windows OS 종류도 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b62ee-110">It also sets Windows OS type.</span></span>
<span data-ttu-id="b62ee-111">두 번째 명령은 disk 개체의 이미지 id와 논리 단위 번호 0을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b62ee-111">The second command sets the image id and the logical unit number 0 for the disk object.</span></span>
<span data-ttu-id="b62ee-112">마지막 명령은 disk 개체를 사용 하 여 리소스 그룹 ' ResourceGroup01 '에 이름이 ' Disk01 ' 인 디스크를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b62ee-112">The last command takes the disk object and creates a disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="b62ee-113">변수</span><span class="sxs-lookup"><span data-stu-id="b62ee-113">PARAMETERS</span></span>

### <span data-ttu-id="b62ee-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b62ee-114">-DefaultProfile</span></span>
<span data-ttu-id="b62ee-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b62ee-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b62ee-116">-디스크</span><span class="sxs-lookup"><span data-stu-id="b62ee-116">-Disk</span></span>
<span data-ttu-id="b62ee-117">로컬 디스크 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b62ee-117">Specifies a local disk object.</span></span>

```yaml
Type: PSDisk
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b62ee-118">-Id</span><span class="sxs-lookup"><span data-stu-id="b62ee-118">-Id</span></span>
<span data-ttu-id="b62ee-119">ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b62ee-119">Specifies the ID.</span></span>

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

### <span data-ttu-id="b62ee-120">-Lun</span><span class="sxs-lookup"><span data-stu-id="b62ee-120">-Lun</span></span>
<span data-ttu-id="b62ee-121">LUN (논리 단위 번호)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b62ee-121">Specifies the logical unit number (LUN).</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b62ee-122">-확인</span><span class="sxs-lookup"><span data-stu-id="b62ee-122">-Confirm</span></span>
<span data-ttu-id="b62ee-123">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="b62ee-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b62ee-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b62ee-124">-WhatIf</span></span>
<span data-ttu-id="b62ee-125">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="b62ee-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b62ee-126">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b62ee-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b62ee-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b62ee-127">CommonParameters</span></span>
<span data-ttu-id="b62ee-128">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b62ee-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b62ee-129">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b62ee-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b62ee-130">입력</span><span class="sxs-lookup"><span data-stu-id="b62ee-130">INPUTS</span></span>

### <span data-ttu-id="b62ee-131">Microsoft. 관리. 디스크</span><span class="sxs-lookup"><span data-stu-id="b62ee-131">Microsoft.Azure.Management.Compute.Models.Disk</span></span>
<span data-ttu-id="b62ee-132">System.webserver 시스템. Null 허용 ' 1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = 중립, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="b62ee-132">System.String System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="b62ee-133">출력</span><span class="sxs-lookup"><span data-stu-id="b62ee-133">OUTPUTS</span></span>

### <span data-ttu-id="b62ee-134">Microsoft. 관리. 디스크</span><span class="sxs-lookup"><span data-stu-id="b62ee-134">Microsoft.Azure.Management.Compute.Models.Disk</span></span>

## <span data-ttu-id="b62ee-135">상속자</span><span class="sxs-lookup"><span data-stu-id="b62ee-135">NOTES</span></span>

## <span data-ttu-id="b62ee-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b62ee-136">RELATED LINKS</span></span>

