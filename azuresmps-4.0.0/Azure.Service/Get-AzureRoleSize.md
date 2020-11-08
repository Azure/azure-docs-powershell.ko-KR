---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 2CBF8DEF-954C-4D9F-B495-C2F76550BC79
online version: ''
schema: 2.0.0
ms.openlocfilehash: 35f7e8a7a08ac2793b7e4aeb8615e5fb8fc1f727
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045615"
---
# <span data-ttu-id="605ce-101">Get-AzureRoleSize</span><span class="sxs-lookup"><span data-stu-id="605ce-101">Get-AzureRoleSize</span></span>

## <span data-ttu-id="605ce-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="605ce-102">SYNOPSIS</span></span>
<span data-ttu-id="605ce-103">현재 구독에 대 한 역할 크기 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="605ce-103">Gets the role size information for the current subscription.</span></span>

## <span data-ttu-id="605ce-104">구문과</span><span class="sxs-lookup"><span data-stu-id="605ce-104">SYNTAX</span></span>

```
Get-AzureRoleSize [[-InstanceSize] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="605ce-105">설명은</span><span class="sxs-lookup"><span data-stu-id="605ce-105">DESCRIPTION</span></span>
<span data-ttu-id="605ce-106">**AzureRoleSize** cmdlet은 현재 구독에 대 한 역할 크기 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="605ce-106">The **Get-AzureRoleSize** cmdlet gets the role size information for the current subscription.</span></span>

## <span data-ttu-id="605ce-107">예제의</span><span class="sxs-lookup"><span data-stu-id="605ce-107">EXAMPLES</span></span>

### <span data-ttu-id="605ce-108">예제 1: 역할 크기 정보 가져오기</span><span class="sxs-lookup"><span data-stu-id="605ce-108">Example 1: Get role size information</span></span>
```
PS C:\> Get-AzureRoleSize

          InstanceSize               : A6
          RoleSizeLabel              :
          Cores                      : 4
          MemoryInMb                 : 28672
          SupportedByWebWorkerRoles  : True
          SupportedByVirtualMachines : True
          OperationDescription       : Get-AzureRoleSize
          OperationId                : c5ed7b3a-03b3-548d-876b-6688c5b29cce
          OperationStatus            : Succeeded

          InstanceSize               : A7
          RoleSizeLabel              :
          Cores                      : 8
          MemoryInMb                 : 57344
          SupportedByWebWorkerRoles  : True
          SupportedByVirtualMachines : True
          OperationDescription       : Get-AzureRoleSize
          OperationId                : c5ed7b3a-03b3-548d-876b-6688c5b29cce
          OperationStatus            : Succeeded
```

<span data-ttu-id="605ce-109">이 명령은 현재 구독에 대 한 역할 크기 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="605ce-109">This command gets role size information for the current subscription.</span></span>

### <span data-ttu-id="605ce-110">예제 2: 역할 크기 정보 가져오기 및 역할 크기 이름 지정</span><span class="sxs-lookup"><span data-stu-id="605ce-110">Example 2: Get role size information and specify the role size name</span></span>
```
PS C:\> Get-AzureRoleSize -InstanceSize A7

          InstanceSize               : A7
          RoleSizeLabel              :
          Cores                      : 8
          MemoryInMb                 : 57344
          SupportedByWebWorkerRoles  : True
          SupportedByVirtualMachines : True
          OperationDescription       : Get-AzureRoleSize
          OperationId                : c5ed7b3a-03b3-548d-876b-6688c5b29cce
          OperationStatus            : Succeeded
```

<span data-ttu-id="605ce-111">이 명령은 지정 된 역할 크기에 대 한 역할 크기 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="605ce-111">This command gets role size information for the specified role size.</span></span>

### <span data-ttu-id="605ce-112">예제 3: 모든 Azure 서비스의 모든 가상 컴퓨터에 대 한 역할 크기 정보 가져오기</span><span class="sxs-lookup"><span data-stu-id="605ce-112">Example 3: Get role size information for all virtual machines in all of the Azure services</span></span>
```
PS C:\> Get-AzureService | Get-AzureVM | Get-AzureRoleSize
```

<span data-ttu-id="605ce-113">이 명령은 모든 Azure services의 모든 가상 컴퓨터에 대 한 역할 크기 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="605ce-113">This command gets role size information for all virtual machines in all of the Azure services.</span></span>

## <span data-ttu-id="605ce-114">변수</span><span class="sxs-lookup"><span data-stu-id="605ce-114">PARAMETERS</span></span>

### <span data-ttu-id="605ce-115">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="605ce-115">-InformationAction</span></span>
<span data-ttu-id="605ce-116">이 cmdlet이 정보 이벤트에 응답 하는 방법을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="605ce-116">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="605ce-117">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="605ce-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="605ce-118">하기로</span><span class="sxs-lookup"><span data-stu-id="605ce-118">Continue</span></span>
- <span data-ttu-id="605ce-119">숨기기</span><span class="sxs-lookup"><span data-stu-id="605ce-119">Ignore</span></span>
- <span data-ttu-id="605ce-120">Inquire</span><span class="sxs-lookup"><span data-stu-id="605ce-120">Inquire</span></span>
- <span data-ttu-id="605ce-121">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="605ce-121">SilentlyContinue</span></span>
- <span data-ttu-id="605ce-122">중지가</span><span class="sxs-lookup"><span data-stu-id="605ce-122">Stop</span></span>
- <span data-ttu-id="605ce-123">대기</span><span class="sxs-lookup"><span data-stu-id="605ce-123">Suspend</span></span>

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

### <span data-ttu-id="605ce-124">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="605ce-124">-InformationVariable</span></span>
<span data-ttu-id="605ce-125">정보 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="605ce-125">Specifies an information variable.</span></span>

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

### <span data-ttu-id="605ce-126">-InstanceSize</span><span class="sxs-lookup"><span data-stu-id="605ce-126">-InstanceSize</span></span>
<span data-ttu-id="605ce-127">역할 크기 이름 (예: ExtraSmall, Small, Large, ExtraLarge, A5, A6, A7)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="605ce-127">Specifies the role size name, for example: ExtraSmall, Small, Large, ExtraLarge, A5, A6, A7.</span></span>

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

### <span data-ttu-id="605ce-128">-프로필</span><span class="sxs-lookup"><span data-stu-id="605ce-128">-Profile</span></span>
<span data-ttu-id="605ce-129">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="605ce-129">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="605ce-130">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="605ce-130">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="605ce-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="605ce-131">CommonParameters</span></span>
<span data-ttu-id="605ce-132">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="605ce-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="605ce-133">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="605ce-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="605ce-134">입력</span><span class="sxs-lookup"><span data-stu-id="605ce-134">INPUTS</span></span>

## <span data-ttu-id="605ce-135">출력</span><span class="sxs-lookup"><span data-stu-id="605ce-135">OUTPUTS</span></span>

## <span data-ttu-id="605ce-136">상속자</span><span class="sxs-lookup"><span data-stu-id="605ce-136">NOTES</span></span>

## <span data-ttu-id="605ce-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="605ce-137">RELATED LINKS</span></span>

[<span data-ttu-id="605ce-138">Get-AzureRole</span><span class="sxs-lookup"><span data-stu-id="605ce-138">Get-AzureRole</span></span>](./Get-AzureRole.md)

[<span data-ttu-id="605ce-139">Get-AzureService</span><span class="sxs-lookup"><span data-stu-id="605ce-139">Get-AzureService</span></span>](./Get-AzureService.md)

[<span data-ttu-id="605ce-140">다운로드-Add-azurevm</span><span class="sxs-lookup"><span data-stu-id="605ce-140">Get-AzureVM</span></span>](./Get-AzureVM.md)


