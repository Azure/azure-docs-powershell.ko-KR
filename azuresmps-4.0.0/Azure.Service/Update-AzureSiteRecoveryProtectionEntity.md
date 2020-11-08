---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 16146A0D-4605-489A-8259-A37BEAC98306
online version: ''
schema: 2.0.0
ms.openlocfilehash: 664c9af9373120f293153a1bbdc65d1a82637631
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046015"
---
# <span data-ttu-id="bde01-101">Update-AzureSiteRecoveryProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="bde01-101">Update-AzureSiteRecoveryProtectionEntity</span></span>

## <span data-ttu-id="bde01-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bde01-102">SYNOPSIS</span></span>
<span data-ttu-id="bde01-103">Azure Site Recovery에서 보호 엔터티의 속성을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="bde01-103">Updates the properties of a protection entity in Azure Site Recovery.</span></span>

## <span data-ttu-id="bde01-104">구문과</span><span class="sxs-lookup"><span data-stu-id="bde01-104">SYNTAX</span></span>

```
Update-AzureSiteRecoveryProtectionEntity -ProtectionEntity <ASRProtectionEntity> [-WaitForCompletion]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="bde01-105">설명은</span><span class="sxs-lookup"><span data-stu-id="bde01-105">DESCRIPTION</span></span>
<span data-ttu-id="bde01-106">**AzureSiteRecoveryProtectionEntity** Cmdlet은 Azure Site Recovery에서 가상 컴퓨터 소유자 정보와 같은 보호 엔터티의 속성을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="bde01-106">The **Update-AzureSiteRecoveryProtectionEntity** cmdlet updates the properties of a protection entity in Azure Site Recovery, such as virtual machine owner information.</span></span>
<span data-ttu-id="bde01-107">이 cmdlet은 vmm 보호 보호 엔터티에 대 한 VMM (가상 컴퓨터 모니터)에 대해서만 지원 됩니다.</span><span class="sxs-lookup"><span data-stu-id="bde01-107">This cmdlet is supported only for Virtual Machine Monitor (VMM) to VMM protected protection entities.</span></span>

## <span data-ttu-id="bde01-108">예제의</span><span class="sxs-lookup"><span data-stu-id="bde01-108">EXAMPLES</span></span>

### <span data-ttu-id="bde01-109">예제 1: 보호 엔터티 업데이트</span><span class="sxs-lookup"><span data-stu-id="bde01-109">Example 1: Update a protection entity</span></span>
```
PS C:\> $Container = Get-AzureSiteRecoveryProtectionContainer
PS C:\> $ProtectionEntity = Get-AzureSiteRecoveryProtectionEntity -ProtectionContainer $Container
PS C:\> Update-AzureSiteRecoveryProtectionEntity -ProtectionEntity $ProtectionEntity
           Name             : 
           ID               : 680ffe0f-6236-465e-8c94-81242fa67e6d
           ClientRequestId  : 2c47e6ce-1460-4187-8a0f-b9073735fa38-2014-12-30 06:44:40Z-P
           State            : NotStarted
           StateDescription : NotStarted
           StartTime        : 
           EndTime          : 
           AllowedActions   : {}
           Tasks            : {}
           Errors           : {}
```

<span data-ttu-id="bde01-110">첫 번째 명령은 **AzureSiteRecoveryProtectionContainer** cmdlet을 사용 하 여 보호 된 컨테이너를 가져온 다음 해당 개체를 $Container 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="bde01-110">The first command gets a protected container by using the **Get-AzureSiteRecoveryProtectionContainer** cmdlet, and then stores that object in the $Container variable.</span></span>

<span data-ttu-id="bde01-111">두 번째 명령은 **AzureSiteRecoveryProtectionEntity** cmdlet을 사용 하 여 $Container에 저장 된 컨테이너에 속하는 보호 된 가상 컴퓨터를 가져온 다음 $ProtectionEntity 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="bde01-111">The second command gets the protected virtual machine that belongs to the container stored in $Container by using the **Get-AzureSiteRecoveryProtectionEntity** cmdlet, and then stores it in the $ProtectionEntity variable.</span></span>

<span data-ttu-id="bde01-112">마지막 명령은 $ProtectionEntity에서 보호 엔터티를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="bde01-112">The final command updates the protection entity in $ProtectionEntity.</span></span>

## <span data-ttu-id="bde01-113">변수</span><span class="sxs-lookup"><span data-stu-id="bde01-113">PARAMETERS</span></span>

### <span data-ttu-id="bde01-114">-프로필</span><span class="sxs-lookup"><span data-stu-id="bde01-114">-Profile</span></span>
<span data-ttu-id="bde01-115">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bde01-115">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="bde01-116">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="bde01-116">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="bde01-117">-ProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="bde01-117">-ProtectionEntity</span></span>
<span data-ttu-id="bde01-118">업데이트할 보호 엔터티를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bde01-118">Specifies a protection entity to update.</span></span>
<span data-ttu-id="bde01-119">**ASRProtectionEntity** 개체를 얻으려면 **Get-AzureSiteRecoveryProtectionEntity** cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="bde01-119">To obtain an **ASRProtectionEntity** object, use the **Get-AzureSiteRecoveryProtectionEntity** cmdlet.</span></span>

```yaml
Type: ASRProtectionEntity
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bde01-120">-WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="bde01-120">-WaitForCompletion</span></span>
<span data-ttu-id="bde01-121">이 cmdlet이 작업을 완료 한 후에 Windows PowerShell 콘솔에 제어를 반환 하는 것을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="bde01-121">Indicates that this cmdlet waits for the operation to complete before it returns control to the Windows PowerShell console.</span></span>

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

### <span data-ttu-id="bde01-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bde01-122">CommonParameters</span></span>
<span data-ttu-id="bde01-123">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="bde01-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bde01-124">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bde01-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bde01-125">입력</span><span class="sxs-lookup"><span data-stu-id="bde01-125">INPUTS</span></span>

## <span data-ttu-id="bde01-126">출력</span><span class="sxs-lookup"><span data-stu-id="bde01-126">OUTPUTS</span></span>

## <span data-ttu-id="bde01-127">상속자</span><span class="sxs-lookup"><span data-stu-id="bde01-127">NOTES</span></span>

## <span data-ttu-id="bde01-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="bde01-128">RELATED LINKS</span></span>

[<span data-ttu-id="bde01-129">Get-AzureSiteRecoveryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="bde01-129">Get-AzureSiteRecoveryProtectionContainer</span></span>](./Get-AzureSiteRecoveryProtectionContainer.md)

[<span data-ttu-id="bde01-130">Get-AzureSiteRecoveryProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="bde01-130">Get-AzureSiteRecoveryProtectionEntity</span></span>](./Get-AzureSiteRecoveryProtectionEntity.md)

[<span data-ttu-id="bde01-131">Set-AzureSiteRecoveryProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="bde01-131">Set-AzureSiteRecoveryProtectionEntity</span></span>](./Set-AzureSiteRecoveryProtectionEntity.md)


