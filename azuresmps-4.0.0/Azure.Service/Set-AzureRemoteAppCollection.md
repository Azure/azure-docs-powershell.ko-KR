---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: 14B4050D-3597-4760-A152-82617B88078D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 291ea94bbdfff1da8d658074ebfb72df8943f0e8
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046053"
---
# <span data-ttu-id="e2f71-101">Set-AzureRemoteAppCollection</span><span class="sxs-lookup"><span data-stu-id="e2f71-101">Set-AzureRemoteAppCollection</span></span>

## <span data-ttu-id="e2f71-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e2f71-102">SYNOPSIS</span></span>
<span data-ttu-id="e2f71-103">RemoteApp 컬렉션의 속성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e2f71-103">Sets the properties of a RemoteApp collection.</span></span>

## <span data-ttu-id="e2f71-104">구문과</span><span class="sxs-lookup"><span data-stu-id="e2f71-104">SYNTAX</span></span>

### <span data-ttu-id="e2f71-105">설명만 (기본값)</span><span class="sxs-lookup"><span data-stu-id="e2f71-105">DescriptionOnly (Default)</span></span>
```
Set-AzureRemoteAppCollection [-CollectionName] <String> -Description <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="e2f71-106">요금제만</span><span class="sxs-lookup"><span data-stu-id="e2f71-106">PlanOnly</span></span>
```
Set-AzureRemoteAppCollection [-CollectionName] <String> -Plan <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="e2f71-107">DomainJoined</span><span class="sxs-lookup"><span data-stu-id="e2f71-107">DomainJoined</span></span>
```
Set-AzureRemoteAppCollection [-CollectionName] <String> -Credential <PSCredential> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="e2f71-108">RdpPropertyOnly</span><span class="sxs-lookup"><span data-stu-id="e2f71-108">RdpPropertyOnly</span></span>
```
Set-AzureRemoteAppCollection [-CollectionName] <String> -CustomRdpProperty <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="e2f71-109">AclLevelOnly</span><span class="sxs-lookup"><span data-stu-id="e2f71-109">AclLevelOnly</span></span>
```
Set-AzureRemoteAppCollection [-CollectionName] <String> -AclLevel <CollectionAclLevel>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="e2f71-110">설명은</span><span class="sxs-lookup"><span data-stu-id="e2f71-110">DESCRIPTION</span></span>
<span data-ttu-id="e2f71-111">**Set-AzureRemoteAppCollection** Cmdlet은 Azure RemoteApp 컬렉션의 속성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e2f71-111">The **Set-AzureRemoteAppCollection** cmdlet sets the properties of an Azure RemoteApp collection.</span></span>

## <span data-ttu-id="e2f71-112">예제의</span><span class="sxs-lookup"><span data-stu-id="e2f71-112">EXAMPLES</span></span>

## <span data-ttu-id="e2f71-113">변수</span><span class="sxs-lookup"><span data-stu-id="e2f71-113">PARAMETERS</span></span>

### <span data-ttu-id="e2f71-114">-AclLevel</span><span class="sxs-lookup"><span data-stu-id="e2f71-114">-AclLevel</span></span>
<span data-ttu-id="e2f71-115">컬렉션에 대 한 ACL (액세스 제어 목록) 수준을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e2f71-115">Specifies the access control list (ACL) level for the collection.</span></span>
<span data-ttu-id="e2f71-116">이 매개 변수에 허용 되는 값은 컬렉션 및 응용 프로그램입니다.</span><span class="sxs-lookup"><span data-stu-id="e2f71-116">The acceptable values for this parameter are: Collection and Application.</span></span>

```yaml
Type: CollectionAclLevel
Parameter Sets: AclLevelOnly
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2f71-117">-CollectionName</span><span class="sxs-lookup"><span data-stu-id="e2f71-117">-CollectionName</span></span>
<span data-ttu-id="e2f71-118">Azure RemoteApp 컬렉션의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e2f71-118">Specifies the name of the Azure RemoteApp collection.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2f71-119">-Credential</span><span class="sxs-lookup"><span data-stu-id="e2f71-119">-Credential</span></span>
<span data-ttu-id="e2f71-120">사용자의 도메인에 Azure RemoteApp 서버에 가입할 수 있는 권한이 있는 서비스 계정의 자격 증명을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e2f71-120">Specifies the credentials of a service account that has permission to join the Azure RemoteApp servers to your domain.</span></span>
<span data-ttu-id="e2f71-121">**PSCredential** 개체를 가져오려면 **Get-Credential** cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="e2f71-121">To obtain a **PSCredential** object, use the **Get-Credential** cmdlet.</span></span>

```yaml
Type: PSCredential
Parameter Sets: DomainJoined
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2f71-122">-CustomRdpProperty</span><span class="sxs-lookup"><span data-stu-id="e2f71-122">-CustomRdpProperty</span></span>
<span data-ttu-id="e2f71-123">드라이브 리디렉션 및 기타 설정을 구성 하는 데 사용할 수 있는 사용자 지정 RDP (원격 데스크톱 프로토콜) 속성을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e2f71-123">Specifies custom Remote Desktop Protocol (RDP) properties which can be used to configure drive redirection and other settings.</span></span> <span data-ttu-id="e2f71-124">자세한 내용은 [Windows Server의 원격 데스크톱 서비스에 대 한 RDP 설정을](https://technet.microsoft.com/library/ff393699(v=ws.10).aspx) 참조 `(https://technet.microsoft.com/library/ff393699(v=ws.10).aspx)` 하세요.  </span><span class="sxs-lookup"><span data-stu-id="e2f71-124">See [RDP Settings for Remote Desktop Services in Windows Server](https://technet.microsoft.com/library/ff393699(v=ws.10).aspx)  `(https://technet.microsoft.com/library/ff393699(v=ws.10).aspx)` for details.</span></span>

```yaml
Type: String
Parameter Sets: RdpPropertyOnly
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2f71-125">-설명</span><span class="sxs-lookup"><span data-stu-id="e2f71-125">-Description</span></span>
<span data-ttu-id="e2f71-126">컬렉션에 대 한 간단한 설명을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e2f71-126">Specifies a short description for the collection.</span></span>

```yaml
Type: String
Parameter Sets: DescriptionOnly
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2f71-127">-계획</span><span class="sxs-lookup"><span data-stu-id="e2f71-127">-Plan</span></span>
<span data-ttu-id="e2f71-128">사용 제한을 정의 하는 Azure RemoteApp 컬렉션에 대 한 계획을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e2f71-128">Specifies the plan for the Azure RemoteApp collection, which defines the usage limits.</span></span>
<span data-ttu-id="e2f71-129">사용할 수 있는 계획을 보려면 **get-help를 AzureRemoteAppPlan** 를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="e2f71-129">Use **Get-AzureRemoteAppPlan** to see the plans available.</span></span>

```yaml
Type: String
Parameter Sets: PlanOnly
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2f71-130">-프로필</span><span class="sxs-lookup"><span data-stu-id="e2f71-130">-Profile</span></span>
<span data-ttu-id="e2f71-131">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e2f71-131">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="e2f71-132">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="e2f71-132">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="e2f71-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2f71-133">CommonParameters</span></span>
<span data-ttu-id="e2f71-134">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e2f71-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2f71-135">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e2f71-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2f71-136">입력</span><span class="sxs-lookup"><span data-stu-id="e2f71-136">INPUTS</span></span>

## <span data-ttu-id="e2f71-137">출력</span><span class="sxs-lookup"><span data-stu-id="e2f71-137">OUTPUTS</span></span>

## <span data-ttu-id="e2f71-138">상속자</span><span class="sxs-lookup"><span data-stu-id="e2f71-138">NOTES</span></span>

## <span data-ttu-id="e2f71-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e2f71-139">RELATED LINKS</span></span>

[<span data-ttu-id="e2f71-140">Get-AzureRemoteAppCollection</span><span class="sxs-lookup"><span data-stu-id="e2f71-140">Get-AzureRemoteAppCollection</span></span>](./Get-AzureRemoteAppCollection.md)

[<span data-ttu-id="e2f71-141">새로운 AzureRemoteAppCollection</span><span class="sxs-lookup"><span data-stu-id="e2f71-141">New-AzureRemoteAppCollection</span></span>](./New-AzureRemoteAppCollection.md)

[<span data-ttu-id="e2f71-142">업데이트-AzureRemoteAppCollection</span><span class="sxs-lookup"><span data-stu-id="e2f71-142">Update-AzureRemoteAppCollection</span></span>](./Update-AzureRemoteAppCollection.md)


