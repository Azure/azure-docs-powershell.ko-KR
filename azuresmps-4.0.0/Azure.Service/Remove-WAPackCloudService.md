---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 1ECF6BB5-3751-4DA0-AC6C-A64F15F46D26
online version: ''
schema: 2.0.0
ms.openlocfilehash: 552c2511a806abb4329860e7c15d8a68b5e03f79
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/08/2020
ms.locfileid: "94047413"
---
# <span data-ttu-id="02396-101">Remove-WAPackCloudService</span><span class="sxs-lookup"><span data-stu-id="02396-101">Remove-WAPackCloudService</span></span>

## <span data-ttu-id="02396-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="02396-102">SYNOPSIS</span></span>
<span data-ttu-id="02396-103">클라우드 서비스 개체를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="02396-103">Removes cloud service objects.</span></span>

## <span data-ttu-id="02396-104">구문과</span><span class="sxs-lookup"><span data-stu-id="02396-104">SYNTAX</span></span>

```
Remove-WAPackCloudService -CloudService <CloudService> [-PassThru] [-Force] [-Profile <AzureSMProfile>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="02396-105">설명은</span><span class="sxs-lookup"><span data-stu-id="02396-105">DESCRIPTION</span></span>
<span data-ttu-id="02396-106">이러한 항목은 더 이상 사용 되지 않으며 향후에 제거 될 예정입니다.</span><span class="sxs-lookup"><span data-stu-id="02396-106">These topics are deprecated and will be removed in the future.</span></span>
<span data-ttu-id="02396-107">이 항목에서는 0.8.1 버전의 Microsoft Azure PowerShell 모듈에 대 한 cmdlet에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="02396-107">This topic describes the cmdlet in the 0.8.1 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="02396-108">Azure PowerShell 콘솔에서 사용 중인 모듈의 버전을 확인 하려면를 입력 `(Get-Module -Name Azure).Version` 합니다.</span><span class="sxs-lookup"><span data-stu-id="02396-108">To find out the version of the module you're using, from the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="02396-109">**Remove-WAPackCloudService** cmdlet은 클라우드 서비스 개체를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="02396-109">The **Remove-WAPackCloudService** cmdlet removes cloud service objects.</span></span>

## <span data-ttu-id="02396-110">예제의</span><span class="sxs-lookup"><span data-stu-id="02396-110">EXAMPLES</span></span>

### <span data-ttu-id="02396-111">예제 1: 클라우드 서비스 제거</span><span class="sxs-lookup"><span data-stu-id="02396-111">Example 1: Remove a cloud service</span></span>
```
PS C:\> $CloudService = Get-WAPackCloudService -Name "ContosoCloudService01"
PS C:\> Remove-WAPackVM -VM $CloudService
```

<span data-ttu-id="02396-112">첫 번째 명령은 **WAPackCloudService** cmdlet을 사용 하 여 ContosoCloudService01 이라는 클라우드 서비스를 가져온 다음 해당 개체를 $CloudService 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="02396-112">The first command gets the cloud service named ContosoCloudService01 by using the **Get-WAPackCloudService** cmdlet, and then stores that object in the $CloudService variable.</span></span>

<span data-ttu-id="02396-113">두 번째 명령은 $CloudService에 저장 된 cloudservice를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="02396-113">The second command removes the cloudservice stored in $CloudService.</span></span>
<span data-ttu-id="02396-114">명령에서 확인 하 라는 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="02396-114">The command prompts you for confirmation.</span></span>

### <span data-ttu-id="02396-115">예제 2: 확인 하지 않고 클라우드 서비스 제거</span><span class="sxs-lookup"><span data-stu-id="02396-115">Example 2: Remove a cloud service without confirmation</span></span>
```
PS C:\> $CloudService = Get-WAPackCloudService -Name "ContosoCloudService02"
PS C:\> Remove-WAPackCloudService -VM $CloudService -Force
```

<span data-ttu-id="02396-116">첫 번째 명령은 **WAPackCloudService** cmdlet을 사용 하 여 ContosoCloudService02 이라는 클라우드 서비스를 가져온 다음 해당 개체를 $CloudService 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="02396-116">The first command gets the cloud service named ContosoCloudService02 by using the **Get-WAPackCloudService** cmdlet, and then stores that object in the $CloudService variable.</span></span>

<span data-ttu-id="02396-117">두 번째 명령은 $CloudService에 저장 된 클라우드 서비스를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="02396-117">The second command removes the cloud service stored in $CloudService.</span></span>
<span data-ttu-id="02396-118">이 명령에는 *Force* 매개 변수가 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="02396-118">This command includes the *Force* parameter.</span></span>
<span data-ttu-id="02396-119">명령에 확인 메시지가 표시 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="02396-119">The command does not prompt you for confirmation.</span></span>

## <span data-ttu-id="02396-120">변수</span><span class="sxs-lookup"><span data-stu-id="02396-120">PARAMETERS</span></span>

### <span data-ttu-id="02396-121">-CloudService</span><span class="sxs-lookup"><span data-stu-id="02396-121">-CloudService</span></span>
<span data-ttu-id="02396-122">클라우드 서비스 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="02396-122">Specifies a cloud service object.</span></span>
<span data-ttu-id="02396-123">클라우드 서비스를 얻으려면 **WAPackCloudService** cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="02396-123">To obtain a cloud service, use the **Get-WAPackCloudService** cmdlet.</span></span>

```yaml
Type: CloudService
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="02396-124">-Force</span><span class="sxs-lookup"><span data-stu-id="02396-124">-Force</span></span>
<span data-ttu-id="02396-125">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="02396-125">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="02396-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="02396-126">-PassThru</span></span>
<span data-ttu-id="02396-127">작업 중인 항목을 나타내는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="02396-127">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="02396-128">기본적으로이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="02396-128">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="02396-129">-프로필</span><span class="sxs-lookup"><span data-stu-id="02396-129">-Profile</span></span>
<span data-ttu-id="02396-130">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="02396-130">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="02396-131">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="02396-131">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="02396-132">-확인</span><span class="sxs-lookup"><span data-stu-id="02396-132">-Confirm</span></span>
<span data-ttu-id="02396-133">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="02396-133">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02396-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="02396-134">-WhatIf</span></span>
<span data-ttu-id="02396-135">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="02396-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="02396-136">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="02396-136">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02396-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02396-137">CommonParameters</span></span>
<span data-ttu-id="02396-138">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="02396-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02396-139">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="02396-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02396-140">입력</span><span class="sxs-lookup"><span data-stu-id="02396-140">INPUTS</span></span>

## <span data-ttu-id="02396-141">출력</span><span class="sxs-lookup"><span data-stu-id="02396-141">OUTPUTS</span></span>

## <span data-ttu-id="02396-142">상속자</span><span class="sxs-lookup"><span data-stu-id="02396-142">NOTES</span></span>

## <span data-ttu-id="02396-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="02396-143">RELATED LINKS</span></span>

[<span data-ttu-id="02396-144">Get-WAPackCloudService</span><span class="sxs-lookup"><span data-stu-id="02396-144">Get-WAPackCloudService</span></span>](./Get-WAPackCloudService.md)

[<span data-ttu-id="02396-145">새로운 WAPackCloudService</span><span class="sxs-lookup"><span data-stu-id="02396-145">New-WAPackCloudService</span></span>](./New-WAPackCloudService.md)


